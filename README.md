# мой первый калькулятор на GO
калькулятор сделанный как тестовое задание для поступления в Kata Academy


> ## Описание задачи
Создай консольное приложение «Калькулятор». Приложение должно читать из консоли введенные пользователем строки, числа, арифметические операции, проводимые между ними, и выводить в консоль результат их выполнения.
Калькулятор можно реализовать обычными функциями либо использовать структуру с методами, здесь это не принципиально.


## Требования:

- ✅ Калькулятор умеет выполнять операции сложения, вычитания, умножения и деления с двумя числами: a + b, a - b, a * b, a / b. Данные передаются в одну строку (смотри пример ниже). Решения, в которых каждое число и арифметическая операция передаются с новой строки, считаются неверными.

```
type your expression
1 + 2
3

type your expression
6 - 8
-2

type your expression
5 * 8
40

type your expression
7 / 2
3

```
    
- ✅ Калькулятор умеет работать как с арабскими (1,2,3,4,5…), так и с римскими (I,II,III,IV,V…) числами.

```
type your expression
V * III
XV

type your expression
X - VIII
II

```

- ✅ Калькулятор должен принимать на вход числа от 1 до 10 включительно, не более. На выходе числа не ограничиваются по величине и могут быть любыми.

```
type your expression
X * X
C

type your expression
10 * 10
100

type your expression
10 * 11
input numbers from 1 to 10 only handled
exit status 1


```

- ✅ Калькулятор умеет работать только с целыми числами.

```
type your expression
1,2 + 1
UNKNOWN NUMBER
exit status 2

type your expression
1.2 + 1
UNKNOWN NUMBER
exit status 2

```

- ✅ Калькулятор умеет работать только с арабскими или римскими цифрами одновременно, при вводе пользователем строки вроде 3 + II калькулятор должен указать на ошибку и прекратить работу.

```
type your expression
3 + II
YOU CAN USE ARABIC OR ROMAN NOT BOTH
exit status 1

type your expression
II + 10
YOU CAN USE ARABIC OR ROMAN NOT BOTH
exit status 1

```

- ✅ При вводе римских чисел ответ должен быть выведен римскими цифрами, соответственно, при вводе арабских — ответ ожидается арабскими.

```
type your expression
1 + 1 
2

type your expression
I + IV
V

```

- ✅ При вводе пользователем не подходящих чисел приложение выводит ошибку в терминал и завершает работу.

```
type your expression
a + i 
UNKNOWN NUMBER
exit status 1

```

- ✅ При вводе пользователем строки, не соответствующей одной из вышеописанных арифметических операций, приложение выводит ошибку и завершает работу.

```
type your expression
2 ^ 2
UNKNOWN OPERATION
exit status 1

```

- ✅ Результатом операции деления является целое число, остаток отбрасывается.

```
type your expression
9 / 2
4

```

- ✅ Результатом работы калькулятора с арабскими числами могут быть отрицательные числа и ноль. Результатом работы калькулятора с римскими числами могут быть только положительные числа, если результат работы меньше единицы, программа должна указать на исключение.

```
type your expression
4 - 7
-3

type your expression
1 - 1
0

type your expression
IV - VII
ROMAN NOTATRION NOT SUPPORT NEGATIVE NUMBERS
exit status 1

```