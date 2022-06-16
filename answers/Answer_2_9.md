#### Вопрос 09

##### Ветвящиеся процессы. Вероятность вырождения.

Если случайная величина $\xi$ целочисленна, т.е. $P(\bigcup_k\{\xi=k\})=1$, то распределение можно характеризовать *производящей функцией*

$$\psi_{\xi}(z)=Mz^{\xi}=\sum z^kP(\xi=k)$$

**Ветвящиеся процессы**

Представим себе частицы, которые могут производить другие частицы того же вида. Пусть в начальный момент времени имеется одна частица ("нулевое поколение"), которая в результате акта "деления" с вероятностью $f_k, k=0,1,2,\dotsc$, переходит в $k$ частиц того же типа, $\sum_{k=0}^{\infty}f_k=1$. Полученные частицы образуют "первое поколение". Каждая из частиц этого поколения ведёт себя точно так же, как исходная частица, независимо от предыстории и судьбы других частиц. В результате получаем нулевое поколение и т.д.

Обозначим $\zeta_n$ число частиц в $n$-м поколении. Для описания последвательности $\zeta_n$ введём в рассмотрение независимые между собой последовательности независимых одинаково распределённых случайных величин $\{\xi_j^{(1)}\}_{j=1}^{\infty},\{\xi_j^{(2)}\}_{j=1}^{\infty},\dotsc$, где $\xi_j^{(n)}$ имеют распределение 

$$P(\xi_j^{(n)}=k)=f_k, k=0,1,\dotsc$$

Тогда последовательность $\zeta_n$ можно представить в виде

$$\zeta_0=1,$$

$$\zeta_1=\xi_1^{(1)},$$

$$\zeta_2=\xi_1^{(2)}+\dotsc+\xi_{\zeta_1}^{(2)},$$

$$\dotsb$$

$$\zeta_n=\xi_1^{(n)}+\dotsc+\xi_{\zeta_n-1}^{(n)}.$$

Это есть сумма случайного числа случайных величин. Т.к. $\xi_1^{(n)},\xi_2^{(n)},\dotsc$ от $\zeta_{n-1}$ не зависят, то по формуле полной вероятности для производящей функции $f_{(n)}(z)=Mz^{\zeta_n}$ получим

$$f_{(z)}(z)=\sum_{k=0}^{\infty}P(\zeta_{n-1}=k)Mz^{\xi_1^{(n)}+\dotsc+\xi_k^{(n)}}=\sum_{k=0}^{\infty}P(\zeta_{n-1}=k)f^k(z)=f_{n-1}(f(z)),$$

где $f(z)=f_{(1)}(z)=Mz^{\xi-1^{(n)}}=\sum_{k=0}^{\infty}f_kz^k$. Пусть $f_n(z)$ означает $n$-ю итерацию функции $f(z)$, т.е. $f_1(z)=f(z), f_2(z)=f(f(z)), f_3(z)=f(f_2(z))$ и т.д. Тогда с помощью инфдукции из соотношений заключаем, что производящая функция $\zeta_n$ равна $n$-й итерации $f(z)$:

$$Mz^{\zeta_n}=f_n(z)$$

Отсюда с помощью дифференцирования в точке $z=1$ легко получить рекуррентные соотношения для моментов $\zeta_n$.

**Вырождение процесса**

Как найти вероятность вырождения процесса? *Вырождение* - событие, состоящее в том, что все $\zeta_n$, начиная с некоторого $n$, равны 0. (Если $\zeta_n=0$, то, очевидно, $\zeta_{n+1}=\zeta_{n+2}=\dotsc=0$, т.к. ($\zeta_{n+1}=0/ \zeta_{n} = 0)=1$.) Обозначим $A_k=\{\zeta_k=0\}$. Тогда вырождение представляет собой событие $\bigcup_{k=1}^{\infty}A_k$. Т.к. $A_n\subset A_{n+1}$, то вероятность вырождения $q$ равна $q=\lim_{n\to \infty} P(A_n)$.

*Теорема*. Вероятность вырождения $q$ равна наименьшему неотрицательному корню уравнения $q=f(q)$.