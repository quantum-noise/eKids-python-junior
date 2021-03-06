# Занятие 3. Модуль __Turtle__

## Теоретическая часть

С помощью Python можно даже рисовать! Что для этого нужно? Выполнить:

```Python
import turtle          # импортировать модуль
t = turtle.Pen()       # создать черепашку
```

__Модуль__ -  функционально законченный фрагмент программы.

`import` - оператор для *подключения* модуля.

Что умеет *черепашка*?

Перемещаться:

```Python
t.forward(50)           # переместить на 50 пикселей вперед
t.backward(10)           # переместить на 10 пикселей назад
```

Метод - функция, принадлежащая *объекту*.
Метод `forward` принимает аргументом число и перемещает черепашку на указанное значение *пикселей* на экране.

Разворачиваться:

```Python
t.left(50)              # поворот в лево на 50°
t.right(90)             # поворот в право на 90°
```

Поднимать и опускать *перо*:

```Python
t.up()                  # подъем пера
t.down()                # опускание пера
```

Если перо поднято, черепашка не будет оставлять след при перемещении.

*Холст* можно очистить двумя методами:

```Python
t.clear()               # очистит экран и вернет черепашку на исходную позицию
t.reset()               # очистит экран но оставит черепашку
```

## Практическая часть

1. Нарисовать квадрат.
1. Нарисовать пунктирную линию.
1. Нарисовать прямоугольник, использовать переменные для хранения значений длин сторон.
1. Нарисовать треугольник.
1. Нарисовать пятиугольник. (Задача со звёздочкой)
1. Нарисовать елочку, использую оператор цикла.