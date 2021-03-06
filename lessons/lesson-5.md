# Занятие 5. Задаем вопросы и проверяем условия

## Теоретическая часть

Логический (булевый) типа данных - примитивный тип данных, принимающий два значения - правда (истина) или ложь.
В языке Python - `True` и `False`.

```Python
a = True                        # значение переменной a - True
```

### Операции сравнения

| Операция | Значение         |
| :------: | :--------------: |
| ==       | Равно            |
| !=       | Не равно         |
| >        | Больше           |
| <        | Меньше           |
| >=       | Больше или равно |
| <=       | Меньше или равно |

Операции сравнения всегда возвращают логический тип, являющийся результатом сравнения:

```Python
'Hello' == 'Hello'              # True
10 == 10                        # True
10 == '10'                      # False, почему?
15 < 10                         # False
0 != 1                          # True
```

### Условный оператор

Оператор сравнения `if then else` - конструкция, позволяющая производить действий после проверки определенного условия.

Проверка одного условия с оператором `if`:

```Python
a = 10
if a == 10:
    print('a равно 10')
print('Привет, мир!')
```

_Обратите внимание, что код, выполняющийся по условию, должен быть в **блоке**!_

_Попробуйте изменить значение переменной **a**, изменится ли вывод на печать?_

Чтобы обработать ситуацию, когда условие не пройдено, воспользуемся оператором `if else`:

```Python
b = 15
if b >= 10:
    print('b больше или равно 10')
else:
    print('b меньше 10')
```

Если обработать нужно множество условий, нам поможет оператор `elif`:

```Python
c = 20
if b <= 10:
    print('с меньше либо равно 10')
elif b <= 20:
    print('с меньше либо равно 20')
elif b <= 30:
    print('с меньше либо равно 30')
else:
    print('c больше 30')
```

_В операторе `if elif else` код выполнится только после первого успешно сравнения и далее сравнения проводится не будут!_

### Объединение условий

Объединить условия можно с помощью операторов `or` (или) и `and` (и):

```Python
a = 10
b = 20
if a == 10 and b == 20:
    print('Вот это да!')
if a > 0 or b > 30:
    print('Не может быть?')
```

С помощью оператора `not` можно _инвертировать_ (поменять) результат логических операций:

```Python
not True                                # False
not 10 == '10'                          # True
```

Скобки `()` помогают группировать логические операции точно так же, как группируются операции математические:

```Python
True == True && not ('a' == 'b' && 10 < 0 )     # True
```

_Обратите внимание, каждый оператор `if` будет делать проеверки независимо!_

_Подумайте, что будет выведено на печать?_

### Таблица _истинности_

| A     | B     | A and B | A or B |
| ----- | ----- | ------- | ------ |
| True  | True  | True    | True   |
| False | True  | False   | True   |
| True  | False | True    | False  |
| False | False | False   | False  |

### Как правильно сравнивать строки и числа

Как мы помним, строки и числа являются разными типами, что влияет и на операцию сравнения:

```Python
10 == '10'                          # False
10 > '10'                           # Ошикба!
```

Для того, чтобы сравнить разные по типу значения, мы можем _привести_ их к единому типу. Помогут нам в этом встроенные функции `str` (строка), `int` (целое число), `float` (действительное число):

```Python
int('10') == 10                     # True
float('20') == 20                   # True
str(10) == '10'                     # True
int('10.0') = 10                    # Ошибка!
```

## Практическая часть

1. Посчитайте результат логический операций

| Выражение                                                 | Результат |
| --------------------------------------------------------- | --------- |
| True and True                                             |           |
| False and True                                            |           |
| 1 == 1 and 2 == 1                                         |           |
| "тест" == "тест"                                          |           |
| 1 == 1 or 2 != 1                                          |           |
| True and 1 == 1                                           |           |
| False and 0 != 0                                          |           |
| True or 1 == 1                                            |           |
| "тест" == "тестирование"                                  |           |
| 1 != 0 and 2 == 1                                         |           |
| "тест" != "тестирование"                                  |           |
| "тест" == 1                                               |           |
| not (True and False)                                      |           |
| not (1 == 1 and 0 != 1)                                   |           |
| not (10 == 1 or 1000 == 1000)                             |           |
| not (1 != 10 or 3 == 4)                                   |           |
| not ("тест" == "тест" and "Python" == "Весело")           |           |
| 1 == 1 and not ("тестирование" == 1 or 1 == 0)            |           |
| "хрум" == "ням" and not (3 == 4 or 3 == 3)                |           |
| 3 == 3 and not ("тест" == "тест" or "Python" == "Весело") |           |