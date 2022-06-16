#### Вопрос 03

##### Случайные блуждания на отрезке. Задача о разорении.

Блуждание на отрезке - классический пример случайного процесса. Частица начинает движение из точки начала координат ($x = 0$) и с равными вероятностями сдвигается влево или вправо на один шаг. 

Блуждание на отрезке лежит в основе задачи о разорении. 

Два игрока играют в безобидную игру (безобидная в том плане, что вероятность выиграть в каждом раунде у двух игроков одинаковая и равна 0.5). Игрок $A$ имеет начальный капитал $a$; игрок $B$ имеет начальный капитал $b$. В каждой партии с вероятностями $\frac{1}{2}$ игрок $A$ выигрывает или проигрывает 1 монету относительно $B$. Блуждание происходит на промежутке $[0; a+b]$. $p$ — вероятность выигрыша $A$, $q$ — вероятность выигрыша $B$. 

(прим. Далее следует решение данной задачи, на всякий случай)

Найдем функцию $g(x)$ 

После первого испытания капитал игрока равен либо  $x − 1$, либо $x + 1$, поэтому при $1 < x < b − 1$ получим уравнение следующее уравнение (1)
$$
g(x) = pg(x + 1) + qg(x − 1)
$$
При $x = 1$ первое испытание может привести к разорению, поэтому
$$
g(1) = pg(2) + q
$$
Кроме того,
$$
g(b − 1) = qg(b − 2)
$$
положим $g(0) = 1;\; g(b) = 0.$ Уравнение (1) есть уравнение в конечных разностях, а условия, определенные ранее служат граничными условиями для $g(x)$. Мы выведем явное выражение для $g(x)$ с помощью метода частных решений. Предположим сначала, что $p\neq q$. Легко проверить, что разностное уравнение (1) имеет два частных решения $g(x) = 1$ и $g(x) =
(\frac{q}{p})^x$.
Отсюда следует, что при произвольных постоянных A и B последовательность
$$
g(x)=A+B(\frac{q}{p})^x
$$
есть решение уравнения (1). Данное уравнение нумеруем как (2). Подберем постоянные A и B так, чтобы выполнялись граничные условия. Это значит, что A и B должны удовлетворять двум линейным уравнениям $A + B = 1$ и $A + B(\frac{q}{p})^b = 0$. Отсюда следует, что 
$$
g(x)=\frac{(\frac{q}{p})^b-(\frac{q}{p})^x}{(\frac{q}{p})^b-1}
$$
Данное уравнение нумеруем как (3). 
то уравнение есть решение разностного уравнения (1), удовлетворяющее граничным условиям. Чтобы доказать, что искомая вероятность разорения равна (3), остается показать,
что решение (3) единственно. Иначе говоря, нужно доказать, что все решения уравнения (1) могут быть записаны в виде (2). Пусть дано произвольное решение уравнения
(1). Мы можем выбрать постоянные A и B так, чтобы (2) совпадало с этим решением
при x = 0 и x = 1. Но по этим двум значениям можно найти все другие значения
с помощью последовательной подстановки в (1) x = 1, 2, 3, . . . . Это значит, что два
решения, совпадающие при x = 0 и x = 1, совпадают тождественно, и поэтому любое
решение имеет вид (2).
Наше рассуждение непригодно при $p = q = \frac{1}{2}$, так как (3) не имеет тогда смысла.
Это происходит потому, что в случае $p = q = \frac{1}{2}$ два частных решения $g(x) = 1$ и
$g(x) =(\frac{q}{p})^x$ совпадают. Однако в этом случае мы имеем второе частное решение
$g(x) = x$ и поэтому $g(x) = A + Bx$ есть решение уравнения (1), зависящее от двух
постоянных. Чтобы удовлетворить граничным условиям, нужно положить A = 1 и
$A + Bb = 0$. Отсюда
$$
g(x)=1-\frac{x}{b}
$$


Таким образом игра с бесконечно богатым соперником неизбежно приводит к разорению, несмотря на то, что внешне игра выглядит безо