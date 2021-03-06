# Подробнее о циклах

## Теоретическая часть

### Итератор

Как мы помним, циклы предназначены для многократного исполнения кода. Мы уже изучили работу оператора цикла `for value in iterator:`, который позволяет «пробежаться» по специальному объекту **итератору**.

**Итератор** - это *объект*, представляющий доступ к коллекции (структуре) данных.

Как можно получить итератор? Можно использовать функцию `range`:

```Python
iterator = range(0, 10)             # Какие числа будет в итератор?

for number in iterator:
    print(number)                   # Вывода на печать чисел из переменной итератора
```

*Структуры данных*, встроенные в Python, имеют внутри себя *итераторы*, что позволяет нам использовать оператор `for` для итерации по спискам, кортежам, словарям:

```Python
list_of_letters = ['a', 'e', 'i', 'o', 'u', 'y']

for letter in list_of_letters:
    print(number)                   # Вывода на печать букв из списка
```

*Важно отметить, что **итератор** не тоже самое что и **список**!*

Воспользовавшись встроенной функцией `list` мы можем *преобразовать* итератор (итерируемую структуру) в список:

```Python
range_iterator = range(5)
tuple_one = (0, 1, 2, 3, 4)
dictionary = {0: 'a', 1: 'b', 2: 'c', 3: 'd', 4: 'e'}

print(list(range_iterator))         # [0, 1, 2, 3, 4]
print(list(tuple_one))              # [0, 1, 2, 3, 4]
print(list(dictionary))             # [0, 1, 2, 3, 4]
```

*Не забывайте, что в словарях **итерация** проходит по **ключам**!*

Подобные функции есть и для остальных, встроенных в Python структур данных.

Функция `tuple` работает аналогично `list`, но преобразует данные в *кортеж*. Работу функции `dict` рассмотрим на одном из дальнейших занятий.

### Оператор цикла **while**

Если оператор `for in` выполняет известное количество итераций, то оператор `while` повторяет выполнение до тех пор, пока не будет выполнено определенное условие:

```Python
condition = True
while condition:
    print('Hello world')
    condition = False
```

*Как вы думаете, сколько раз выполнится код в блоке цикла?*

Оператор `while` удобно использовать, когда нужно рассчитать какую-либо величину за заранее неизвестное количество повторений.

### Оператор прерывания цикла **break**

Иногда решение какой-либо задачи, решаемой в цикле, находится раньше, чем пройдут все итерации цикла. Тогда работу цикла можно прервать с помощью оператора `break`:

```Python
for i in range(10):
    print(i)
    break
```

*Цикл выполнится один раз и прервется.*

```Python
a = 0
while True:
    if a >= 10:
        break
    a += 1
```

*Цикл прервется после того, как значение переменной `a` станет больше либо равным 10.*

## Практическая часть

1. Рассчитать за сколько лет, вклад в 1.000 рублей выросте до 1.000.000 если процент по вкладу составляет 5% годовых.