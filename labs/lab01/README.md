# Lab 1: Advanced Python

Лаба: http://cs.mipt.ru/python/lessons/lab1.html.

В качестве ДЗ достаточно решить две задачи, причём одна задача должна быть номер 1 или 2, а другая — номер 3 или 4 (то есть, например, можно выбрать задачи 1 и 3).
А решение надо [*залить в свой репозиторий на Гитхабе*](../docs/git-how-to)!


## Задача 1

Постройте график функции $f(x)$ и решите уравнение $f(x) = c$ при всех значениях $c \in \mathbb R$ (надо просто выписать ответ глядя на график).

$$
  f(x) = \frac{-x^2 + 3x - 1}{x}
$$


## Задача 2

Постройте график функции $f(x)$ и найдите все точки её локального экстремума (надо просто выписать ответ глядя на график).

$$
  f(x) = \frac{x^3 - 4}{(x - 1)^3}
$$


## Задача 3

Постройте график функции $f(x)$ на отрезке $[-6, 6]$:

$$
  f(x) = 1.1^{-2x} \cdot \sin^2 x
$$


## Задача 4

Постройте график функции $f(x)$ на отрезке $[-6, 6]$:

$$
  f(x) = \arcsin \left( \frac{2 |x|}{1 + x^2} \right)
$$


## Задача 5*

Во время лабораторной работы, посвящённой изучению изменения агрегатного состояния веществ, молодой любитель физики провёл следующий эксперимент.

Взял порцию некоторого вещества массой 100 грамм в твёрдом состоянии при комнатной температуре 20 °C, расплавил и потом ещё нагрел до 80 °C.
После этого выключил нагрев — началось охлаждение — и через каждые полминуты считывал по градуснику показания температуры.

Были получены следующие результаты (значения в первой строчке — время от начала охлаждения, во второй — соответствующая температура):
```
Time, s
0 30 60 90 120 150 180 210 240 270 300 330 360 390 420 450 480 510 540 570 600 630 660 690 720 750 780 810 840 870 900

Temperature, °C
79 77 74 69 65 60 60 60 60 60 60 60 60 60 60 60 60 60 60 60 58 56 49 46 42 40 33 31 27 23 21
```

Считая погрешность измерения температуры равной 2 °C (такая большая, потому что, кроме цены деления градусника 1 °C, хочется учесть ещё тот факт, что экспериментатору не так просто было быстро переводить взгляд с секундомера на градусник), отметьте на графике точки с погрешностями и начертите аппроксимационную кривую всего процесса.

P.S.

Чему равна удельная теплоёмкость вещества в твёрдом состоянии, если известно, что удельная теплота плавления $\lambda = 1.5 \cdot 10^5$ Дж/кг?


## Задача 6*

Постройте график функции [Вейерштрасса](https://ru.wikipedia.org/wiki/%D0%A4%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D1%8F_%D0%92%D0%B5%D0%B9%D0%B5%D1%80%D1%88%D1%82%D1%80%D0%B0%D1%81%D1%81%D0%B0) на отрезке $[−2, 2]$.
