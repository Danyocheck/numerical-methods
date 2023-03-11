# numerical-methods
# Метод Адамса
Метод Адамса второго порядка - это численный метод решения дифференциальных уравнений, который используется для приближенного нахождения значений решения уравнения на равномерной сетке. Этот метод является явным и имеет порядок точности O(h^2), где h - шаг сетки.

Рассмотрим дифференциальное уравнение вида y' = f(x,y), где $y(x_0) = y_0$, и пусть даны значения решения на первых двух точках сетки: y_0 и y_1. Тогда для нахождения значения $y_2$ на следующей точке сетки используется следующая формула:

y_2 = y_1 + h/2[3f(x_1, y_1) - f(x_0, y_0)]

Здесь h - шаг сетки, $x_1 = x_0 + h$, а f(x,y) - функция правой части дифференциального уравнения.

Далее, для нахождения значений на следующих точках сетки используется формула:

$\frac {y_{i+1} - y_i}{h} = \frac {3}{2} f_i - \frac {1}{2} f_{i-1}$

Эта формула является обобщением формулы для $y_2$ и позволяет находить значения решения на следующих точках сетки.

В целом, метод Адамса второго порядка позволяет находить приближенное решение дифференциальных уравнений на равномерной сетке, используя лишь начальные значения решения. Однако, для обеспечения точности решения, необходимо выбирать достаточно малый шаг сетки.




