# Lab 3: Функции, списки, файлы и черепаха

Лаба: http://cs.mipt.ru/python/lessons/lab3.html.

В качестве ДЗ достаточно решить *четыре* задачи: одну по функциям, одну по спискам, одну по файлам и одну по Черепахе.


## Функции

### Задача Ф1 (График)

Начертите график какой-нибудь функции с помощью функции `plot` библиотеки `matplotlib`, но при построении графика задайте:
* тип линии (например, сплошная или пунктирная)
* ширину линии
* цвет линии
* тип точек, по которым строится график ("маркеры")
* размер точек
* цвет точек
* ширину границы точек
* цвет границы точек

<p align="center">
  <img src="https://github.com/Alvant/AscendingPython/assets/15067981/727cb8a9-a77b-4aed-ad33-12858bcddfcb" alt="Result of plt.plot with many params" />
</p>
<p align="center">
  <em>
    Пример графика.
  </em>
</p>


### Задача Ф2 (Сигнатура, или "Шапка" функции)

Напишите функцию `f`, которая печатает на экране одну строку и которую можно бы было вызывать следующим образом:

```python
# Определение функции f от скольких-то параметров
# ...

f('a', 'b')                 # a b b c a
f('b', 'a')                 # b b a c a
f('a', 'b', 'f')            # a b b f a
f('a', 'b', d='d')          # a d b c a
f('*', '*', '*', '*', '*')  # * * * * *
```


### Задача Ф3* (Непостоянная функция)

Напишите функцию, которая печатает на экране строку, причём результат (конкретный вывод) чередуется в зависимости от вызова.
То есть: первый раз вызвали функцию — на выходе одна строка, второй раз вызвали — другая, ещё один вызов — и функция выводит первоначальную строчку, и так далее.

Пример:

```python
# Определение "непостоянной" функции-флюгера vane_print
# ...

# Использование функции (после вызова в комментарии указан вывод)
vane_print()  # попка
vane_print()  # дурак
vane_print()  # попка
vane_print()  # дурак
```


## Списки + Файлы




## Черепаха

<p align="center">
  <img src="https://github.com/Alvant/AscendingPython/assets/15067981/fd942424-39d1-4bde-81a7-8feb87399df1" alt="Waltz of the Turtles" title="Python + Turtle" data-canonical-src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdXhxM3U5eDM0OWdlN2R2YzZrdGw0MnBoOWdjZzQzejNnbTAya2FudCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bRwbmwcWANmGGbTofK/giphy.gif" />
</p>
<p align="center">
  <em>
    Вальс черепашек
	(<a href="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdXhxM3U5eDM0OWdlN2R2YzZrdGw0MnBoOWdjZzQzejNnbTAya2FudCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bRwbmwcWANmGGbTofK/giphy.gif">gif</a>).
  </em>
</p>




<p align="center">
  <img src="https://github.com/Alvant/AscendingPython/assets/15067981/f2f41348-f611-4ccf-8b62-e02098e1f2f5" alt="The Call of Cthulhu" title="Python + Turtle" data-canonical-src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdG0wZ2x1OHdxdmRqM3E0ZGVjNWpxYXR4ZDlub3dwaW1ubzJyMHB0aCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/rYSPkh3G3nnuPfnsIu/giphy.gif" />
</p>
<p align="center">
  <em>
    Вызов Ктулху
	(<a href="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdG0wZ2x1OHdxdmRqM3E0ZGVjNWpxYXR4ZDlub3dwaW1ubzJyMHB0aCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/rYSPkh3G3nnuPfnsIu/giphy.gif">gif</a>).
  </em>
</p>




<p align="center">
  <img src="https://github.com/Alvant/AscendingPython/assets/15067981/d8af28ea-3d40-48b2-85a8-fc5890af31ff" alt="Chemical Flask" title="Python + Turtle" data-canonical-src="https://media.giphy.com/media/Ka8H6rOxpwKjIc7xs9/giphy.gif" />
</p>
<p align="center">
  <em>
    Химическая колба
    (<a href="https://media.giphy.com/media/Ka8H6rOxpwKjIc7xs9/giphy.gif">gif</a>).
  </em>
</p>




<p align="center">
  <img src="https://github.com/Alvant/AscendingPython/assets/15067981/907d363d-6664-4686-99cd-d5fabdec38ab" alt="Flower" title="Python + Turtle" data-canonical-src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExY2VqeHBoa3U4dWpheWF2NWw3MnhqYjQ3amJyMDBndHlyNm50aGl1eCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/m1qTiiEgLRdDNK6GbI/giphy.gif" />
</p>
<p align="center">
  <em>
	Цветочек
    (<a href="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExY2VqeHBoa3U4dWpheWF2NWw3MnhqYjQ3amJyMDBndHlyNm50aGl1eCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/m1qTiiEgLRdDNK6GbI/giphy.gif">gif</a>).
  </em>
</p>