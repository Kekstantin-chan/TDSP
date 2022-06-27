#### Задача 2
##### Цепи Маркова

**Пример 1**
Найдем стационарное распределение:

<img src="Practice_2/image-20220626192137192.png" alt="image-20220626192137192" style="zoom: 80%;" />

Матрица переходов 
$$
P=(p_{ij})=
\begin{pmatrix}
0,3 & 0.7 \\
1 & 0
\end{pmatrix}
$$
Стационарное распределение будет иметь вид $\pi = (\pi_1, \pi_2)$. Мы знаем, что вектор распределения вероятностей на любом шаге можно найти по рекуррентной формуле $p(n)=p(n-1)P$. Т.к. по своству стационарного распределения оно обозначает, что распределение вероятностей на шаге $n \rightarrow \infin$ не отличается от распределения на шаге $n+1 \rightarrow \infin$. Получаем что
$$
\pi=\pi \cdot P \\
\begin{cases}
0,3\pi_1+\pi_2=\pi_1 \\
0,7\pi_1+0\pi_2=\pi_2 \\
\pi_1 + \pi_2 = 1
\end{cases}
$$
Решив систему получим 
$$
\begin{cases}
\pi_1=\frac{10}{17}\\
\pi_2=\frac{7}{17}
\end{cases}
$$
*Переводя на человеческий язык*: данная система, независимо от начального состояния, на шаге $n \rightarrow \infin $ будет с вероятностью $\pi_1$ в состоянии $S_1$ (или с вероятностью $\pi_2$ в состоянии $S_2$)

**Пример 2**

Задана матрица переходных вероятностей
$$
P =
\begin{pmatrix}
0.4 & 0.6 \\
0.3 & 0.7
\end{pmatrix}
$$

*Задача*:
Найти матрицу $P_2$ (*простыми словами*, найти распределение в каком состоянии будет система на 2ом шаге)

*Решение*:
Найдем матрицу $P_2$ 
$$ 
P_2 = P_1 \cdot P_1 = (\text{*перемножение матриц*}) = 
\begin{pmatrix}
0.34 & 0.66 \\
0.33 & 0.67
\end{pmatrix}
$$

*Задача*:
Найдем распределение вероятностей по состояниям системы в момент $t=2$. Начальное распределение $q=(0,1;0,9)$ (система с вер. 0.1 начинает работу с состояния 1, и с вер. 0.9 с состояния 2)

*Решение*: 
$$
p(2)=q\cdot P_2 = (0.1, 0.9)
\begin{pmatrix}
0.34 & 0.66 \\
0.33 & 0.67
\end{pmatrix} 
= (0.331, 0.669) 
$$
Система с вероятностью 0.669 (при начальном состоянии (0.1, 0.9)) будет в состоянии 2 после двух шагов.

*Задача*:
Найдем стационарное распределение системы (вероятностное распределение в каком состоянии будет система после $n \rightarrow \infin$ шагов при любом начальном состоянии)

*Решение*:
Т.к при очень большом n значения $p(n)$ и $p(n+1)$ стремятся к одному значению (они бесконечно очень близки). А это значит что(сделам замену)
$$
p(n+1)=p(n)P \\
\pi=\pi P
$$
где $\pi$ - стационарное распределение.
Это $\pi$ можно найти решив систему. В данном случае 
$$
\begin{cases}
\pi_1=0.4\pi_1 + 0.3\pi_2\\
\pi_2=0.6\pi_1 + 0.7\pi_2\\
\pi_1+\pi_2=1
\end{cases}
$$
Решив эту систему получим 
$$
\pi=\{\frac{1}{3};\frac{2}{3}\}
$$
Это означает что система, на бесконечно большом шаге, будет с вероятностью $\frac{2}{3}$ в состоянии 2