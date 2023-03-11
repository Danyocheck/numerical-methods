# Метод Адамса
Метод Адамса второго порядка - это численный метод решения дифференциальных уравнений, который используется для приближенного нахождения значений решения уравнения на равномерной сетке. Этот метод является явным и имеет порядок точности $O(h^2)$, где h - шаг сетки.

Рассмотрим дифференциальное уравнение вида y' = f(x,y), где $y(x_0) = y_0$, и пусть даны значения решения на первых двух точках сетки: y_0 и y_1. Тогда для нахождения значения $y_2$ на следующей точке сетки используется следующая формула:

$y_2 = y_1 + \frac {h}{2}[3f(x_1, y_1) - f(x_0, y_0)]$

Здесь h - шаг сетки, $x_1 = x_0 + h$, а f(x,y) - функция правой части дифференциального уравнения.

Далее, для нахождения значений на следующих точках сетки используется формула:

$\frac {y_{i+1} - y_i}{h} = \frac {3}{2} f_i - \frac {1}{2} f_{i-1}$

Эта формула является обобщением формулы для $y_2$ и позволяет находить значения решения на следующих точках сетки.

В целом, метод Адамса второго порядка позволяет находить приближенное решение дифференциальных уравнений на равномерной сетке, используя лишь начальные значения решения. Однако, для обеспечения точности решения, необходимо выбирать достаточно малый шаг сетки.



# Метод Рунге-Кутта
Метод Рунге-Кутта - это численный метод решения дифференциальных уравнений, который используется для приближенного нахождения значений решения на равномерной сетке. Этот метод имеет порядок точности $O(h^2)$, где h - шаг сетки.

Пусть дано дифференциальное уравнение вида y' = f(x,y), где $y(x_0) = y_0$, и пусть заданы начальные значения $y_0$ на первой точке сетки. Тогда для нахождения значений на следующей точке сетки используется формула:

$y_{i+1} = y_i + \frac{h}{2}(\alpha_1 + \alpha_2)$

где h - шаг сетки, $x_i+1 = x_i + h$, \alpha_1 = $f(x_i, y_i), \alpha_2 = f(x_i+1, y_i + h * \alpha_1)$ - вычисленный с помощью $\alpha_1$ наклон второго порядка на отрезке $[x_i, x_i+1]$.

Для нахождения $\alpha_2$ используется метод Эйлера, где на отрезке $[x_i, x_i+1]$ происходит движение из начальной точки $(x_i, y_i)$ с шагом $h * \alpha_1$.

Таким образом, значения на каждой следующей точке сетки вычисляются последовательно с помощью выражения, которое зависит от значений функции в предыдущих точках. Начальные значения задаются методом, который обеспечивает более высокую точность, например, методом Эйлера или методом Рунге-Кутта первого порядка.

Метод Рунге-Кутта позволяет находить приближенное решение дифференциальных уравнений на равномерной сетке с достаточно высокой точностью. Однако, для обеспечения точности решения, необходимо выбирать достаточно малый шаг сетки.


# Интерполяция полиномом
Интерполяция полиномом - это метод аппроксимации функции многочленом на заданном интервале, когда известны значения функции в некоторых точках. Идея метода заключается в нахождении многочлена степени n, который проходит через эти точки.

$P_n(x_i) = f(x_i) = f_i$

Многочлен интерполяции может быть записан в следующем виде:

$P_n(x) = a_0 + a_1x + a_2x^2 + ... + a_n*x^n$,

где $a_0, a_1, ..., a_n$ - коэффициенты многочлена, x - независимая переменная, а n - степень многочлена.

Для нахождения коэффициентов многочлена необходимо решить систему линейных уравнений, где количество уравнений равно количеству точек, в которых известны значения функции. Значения коэффициентов многочлена могут быть найдены, используя методы решения систем линейных уравнений, такие как метод Гаусса или метод прогонки.

Полученный многочлен интерполяции может быть использован для вычисления значений функции в любых точках на заданном интервале. Однако, стоит отметить, что точность интерполяции зависит от степени многочлена и расположения точек, в которых известны значения функции. В случае, если точки расположены неравномерно или на интервале присутствуют особые точки, такие как точки разрыва или различные асимптоты, может потребоваться использование специальных методов интерполяции.
