#### Вопрос 07

##### Тождество Вальда. Схема цепной реакции.

Пусть $S_{\nu} = \xi_1+ \dotsc \xi_{\nu}$ - сумма случайного числа случайных величин.

**Тождество Вальда**. Если случайные величины $\xi_1,\xi_2,\dotsc$ независимы и одинаково распределены, $M|\xi_k|<\infty$, а случайная величина $\nu$ не зависит от будущего, $M\nu<\infty$, то $MS_{\nu}=M\xi_1M\nu$. (Тождество Вальда является следствием теоремы Колмогорова-Прохорова)

(*Комментарий с notion*: Матожидание суммы случайного числа $\nu$ *одинаковых* случайных величин $\xi$ равно произведению матожидания самой случайной величины $\xi$ на матожидание количества таких случайных величин)

**Схема цепной реакции**

Пусть мы имеем в качестве исходной одну частицу, которая либо исчезает с вероятностью $q$, либо превращается в $m$ таких же частиц с вероятностью $p=1-q$. Каждая частица нового поколения ведёт себя таким же образом независимо от судьбы остальных частиц. Чему равно математическое ожидание числа $\zeta_n$ частиц в $n$-м поколении? ($M\zeta_n - ?$)

Рассмотрим "двойную" последовательность $\{\xi_k^{(n)}\}_{k=1}^{\infty},_{n=1}^{\infty}$ независимых одинаково распределённых случайных величин, принимающих значения $m$ и 0 с вероятностями $p$ и $q$. Очевидно, что последовательности $\{\xi_k^{(1)}\}_{k=1}^{\infty},\{\xi_k^{(2)}\}_{k=2}^{\infty},\dotsc$ будут независимыми между собой. С помощью этих последовательностей случайные величины $\zeta_n(\zeta_0=1)$ можно представить в виде:

$$\zeta_1=\xi_{\zeta_0}^{(1)}=\xi_1^{(1)}$$

$$\zeta_2=\xi_1^{(2)}+\dotsc+\xi_{\zeta_1}^{(2)}$$

$$\dotsb$$

$$\zeta_n=\xi_1^{(n)}+\dotsc+\xi_{\zeta_{n-1}}^{(n)}$$

$\zeta_i$ - количество частиц в $i$-м поколении. В равенстве для $\zeta_n$ число слагаемых $\zeta_{n-1}$ есть число "частиц-родителей". Т.к. последовательность $\{\xi_k^{(n)}\}$ не зависит от $\zeta_{n-1}$ и $M\xi_k^{(n)}=pm$, то в силу тождества Вальда 

$$M\zeta_n=M\xi_1^{(n)}M\zeta_{n-1}=pmM\zeta_{n-1}=(pm)^n$$

*(Чуть более подробный вывод формулы из notion)*

$M|\xi_k^{(\cdot)}|<\infty$

$M\xi_k^{(\cdot)}=0\cdot q + m\cdot p=mp<\infty$ - матожидание каждой из случайных величин($M\xi_n$ в тождестве Вальда)

$M\zeta_1=mp<\infty$

$M\zeta_1=mp\cdot mp=(mp)^2<\infty$(количество случайных величин ($\nu$ в тождестве Вальда) равно $\zeta_1$)

$M\zeta_3 = M(\xi_1^{(3)} +\dotsc+ \xi_{\zeta_2}^{(3)})= M\xi_k^{(3)}\cdot M\zeta_2 = mp\cdot (mp)^2 = (mp)^3$

$\dotsc$

$M\zeta_n = (mp)^n$