Теорема 8 (Эргодическая). 

(1) Существует состояние $E_s$ такое, что время $\tau^{(s)}$ возвращения в $E_s (P(\tau^{(s)}= n) = f_s(n))$ имеет конечное математическое ожидание $E\tau^{(s)} < \infty$.

(2) Цепь неразложима

(3) Цепь непериодична

Условия (1-3) необходимы и достаточны для того, чтобы при любых $i$ и $j$ существовали не зависящие от $i$ положительные пределы $\lim\limits_{n\rightarrow\infty} p_{ij}(n) = \pi_j >0, i,j =0,1,2,\ldots$

Числа $\{\pi_j \}$ являются единственным в классе последовательностей, образующих абсолютно сходящиеся ряды, решением системы уравнений: $\begin{cases} \sum \limits_{j=0}^∞ \pi_j=1 \\ \pi_j=\sum \limits_{k=0}^∞\pi_k p_{kj};\;j=0,1,2...\end{cases}$(2)

Кроме того, $E_{t^{(s)}}<∞$ при всех $j$ и числа $\pi_j=(Et^{(j)})^{-1}$ допускают представление $\pi_j=(Et^{(j)})^{-1}=(Et^{(s)})^{-1}\sum \limits_{k=1}^∞P_s(k,j)$ при любом s

Цепь, обладающая свойством (1) — эргодическая

Распределение $\{\pi_j\}$-стационарное

Свойство (2) выражает инвариантность распределения относительно переходных вероятностей

Числа $\pi_j$ есть, по существу, вероятности попадания системы в состояние $E_j$ через большой интервал времени. При этом оказывается, что эти вероятности не зависят от начального состояния системы. Система "забывает", откуда началось движение. Распределение {$\pi_j$} называют стационарным или инвариантным.

Пример

$ \pi=\begin{pmatrix} 0.2&0.3&0.5\\ 0.1&0.6&0.3\\ 0.2&0.7&0.1\end{pmatrix} $, 

Данные строки умножаем на соответствующий $p_i$, где $i$ номер столбца и приравниваем к $p_j$, где $j$ - номер строки. Также учитываем условие, что сумма вероятностей должна равняться единице.

$\begin{cases} p_1+p_2+p_3 = 1\\ 0.2p_1+0.1p_2+0.2p_3 = p_1\\ 0.3p_1+0.6p_2+0.7p_3 = p_2\\ 0.5p_1+0.3p_2+0.1p_3 = p_3\end{cases}$

При возведении матрицы переходов ($\pi$) во 2 степень получим вероятность попадания из одной точки в другую за 2 шага, а при возведении в большие степени (условно говоря, стремящиеся к бесконечности) вероятности в ней будут становиться всё более и более равными по столбцам и будут стремиться к эргодическим вероятностям ($p_j$).