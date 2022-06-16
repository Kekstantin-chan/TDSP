#### Вопрос 05

##### Задача о выборе наибольшего приданого (о выборе невесты)

Условие задачи звучит так:

Король, на испытании кандидатов на пост придворного мудреца, предлагает ему женитьбу на молодой придворной даме, имеющей наибольшее приданое. Сумма приданого записывается на билетиках; они перемешиваются. Наудачу вытягивается билетик, и мудрец должен решить, является ли это приданое наибольшим или нет, либо же отказаться от решения.

При правильном решении мудрец побеждает, при неправильном — ничего. При отказе от суммы, указанной на первом билете, мудрец должен вытянуть второй билет и так же принять его или же от него отказаться, пока не сделает выбор или не отвергнет все приданые.

При дворе короля 100 дам, все их приданые различны. Как должен действовать мудрец?

(прим. далее идет решение данной задачи)

Оптимальной стратегией является пропуск первых $s-1$ билетов и выбрать первый максимальный номер после них. Мы выберем максимальное приданое на $і$-м шагу, если вероятность правильного решения при оптимальной стратегии и более позднем вытягивании. Формально: остановится на максимальном номере при $i$-м вытягивании, если
$$
P(выиграть\;при\; i-м\; вытягивании) >\\ P(выиграть\;при\; оптимальной\; стратегии,\; начиная \;с\; i+1\; вытягивания)\;\;(1)
$$
Покажем, что вероятность в правой части (1) убывает, когда $i$ возрастает, а вероятность в левой части (1) возрастает с возрастанием $i$, и после которого предпочтительнее удержать максимальное приданное, нежели продолжать испытание. Вычисляя затем вероятность выигрыша для такой стратегии, найдем оптимальный выбор значения $s$. 

Вероятность того, что на $i$-м максимальное приданное больше всех имеющихся, равна вероятности того, что наилучший номер находится на одном из первых $i$ билетов, а именно равна $\frac{i}{n}$, что является строго возрастающей от $\frac{1}{n}$ до 1 функции от $i$. Поэтому значение $\frac{i}{n}$ в какой-то точке превосходит вероятность выигрыша при продолжении испытании. Сосчитаем вероятность выигрыша для такой стратегии. Вероятность правильного решения есть  вероятность появления ровно одного лидера между  $s$-м шагом и $n$-м. Вероятность того, что наилучший билет появился на $k$-м шагу, равна $\frac{1}{n}$. Вероятность того, что максимум первых $k-1$ номеров появился среди первых $s-1$ номеров, есть $\frac{s-1}{k-1}$. Произведение $\frac{s-1}{n(k-1)}$ дает вероятность того, что выиграем при выборе $k,\;s\leq k\leq n.$ Суммируя эти числа, получим вероятность $\pi(s,n)$ получения наилучшего приданного при оптимальной стратегии
$$
\pi(s,n)=\frac{1}{n}\sum\limits_{k=s}^n\frac{s-1}{k-1}=\frac{s-1}{n}\sum\limits_{k=s-1}^{n-1}\frac{1}{k}=\\
=\frac{s-1}{n}(\frac{1}{s-1}+\frac{1}{s}+\dots+\frac{1}{n-1}),\;1\leq s\leq n.\;\;(2)
$$
 Оптимальное значение $s$ есть такое значение, для которого имеет место неравенство (1), т.е. это наименьшее $s$, для которого 
$$
\frac{s}{n}>\pi(s+1,n)=\frac{s}{n}(\frac{1}{s}+\frac{1}{s+1}+\dots+\frac{1}{n-1})
$$