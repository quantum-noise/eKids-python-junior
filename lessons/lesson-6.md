# Делаем вычисления проще с Python

## Теоретическая часть

### Математические операции

В языке Python доступны следующие математические операции:

| Операция | Название              |
| -------- | --------------------- |
| +        | Сложение              |
| -        | Вычитание             |
| *        | Умножение             |
| /        | Деление               |
| //       | Деление с округлением |
| %        | Остаток от деления    |
| **       | Возведение в степень  |

Проверить работу операций можно введя следующие команды в IDLE:

```Python
a = 3
b = 10
print(10 + 3)                       # 13
print(3 - 10)                       # -7
print(3 * 10)                       # 30
print(10 / 3)                       # 3.3333333333333335
print(10 // 3)                      # 3
print(10 % 3)                       # 1
print(10 ** 3)                      # 1000
```

*Обратите внимание на результат операции 10 / 3. Как вы думаете, почему именно такой результат?*

### Присваивание с операцией

Иногда возникает необходимость присвоить переменной новое значение, являющееся результатом какой-нибудь операции над старым. Для это можно воспользоваться специальным синтаксисом `[операция]=`

```Python
a = 10
a += 10                             # a = a + 10
print(a)                            # 20
a /= 2                              # a = a / 2
print(a)                            # 10
```

## Практическая часть

*Все задания необходимо выполнять и сохранять в отдельных файлах.*

1. Вывести на печать все числа кратные `3` в диапазоне от 0 до 50.

2. Найти и вывести на печать сумму всех чисел от 0 до 200.

3. Найти площадь круга с диаметром 12.8. Значение числа `π` можно взять в модуле Math. Площадь круга находится по формуле `S = πr²`.

    ```Python
    import math
    print(math.pi)                      # 3.141592653589793
    ```

4. Создать и вывести на печать словарь, в котором ключи это числа от 3 до 10, а значения - список чисел, которые делятся без остатка на ключ в диапазоне от 3 до 100 включительно. Пример части словаря:

    ```Python
    {
        ...
        10: [10, 20, 30, 40, 50, 60, 70, 80, 90, 100]
    }
    ```

5. Построить с помощью модуля turtle график (часть графика для `x > 0`) для функции `y = x²`. (Домашнее задание)
