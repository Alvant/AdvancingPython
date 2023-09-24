# Lab 4: Рекурсия, "несписки", строки и картинки на выставку

Лаба: http://cs.mipt.ru/python/lessons/lab4.html.

В качестве ДЗ достаточно решить *четыре* задачи: одну по функциям, одну по "неспискам", одну по строкам и одну по "Картинкам на выставку".


## Рекурсия

### Задача F1 (Факториал)

Напишите рекурсивную функцию, вычисляющую факториал числа:

```python
def factorial(n):
    # ... Рекурсивная функция ...

print(factorial(3))  # 6
```




## "Несписки"




## Строки


### Задача S... (Заборчик в Зазеркалье)

Напишите функцию, принимающую на вход строку и возвращающую новую строку, построенную по исходной, так что "маленькие" буквы становятся "большими" и наоборот.

```python
def mirror_case(s):
    # Меняет регистр с маленького на большой и наоборот

print(mirror_case(""))
```


### Задача S... (...)

Напишите функцию, которая получает на вход несколько фактов о человеке и составляет по ним короткое связное описание.

Параметры функции:
* имя (строка)
* возраст (целое число)
* средняя оценка по предметам (число с плавающей точкой)
* хобби (список строк)
* любимое блюдо (строка)

Функция возвращает одну строку – связный "рассказ" о человеке.
Рассказ строится по шаблону, суть которого лучше увидеть на примере:

```python
def make_description(name, age, grade, hobbies, favourite_food):
    # Составляет описание

print(
    make_description(
        name='Nick', age=18, grade=7.4, favourite_food='ролл Калифорния',
        hobbies=['бадминтон', 'бас-гитара', 'прокрастинация'],
    )
)
```

<p align="center">
  <img src="./docs/images/Nick_Fact_Screen.jpg" alt="Task sponsor: Lollipop Chainsaw" />
</p>
<p align="center">
  <em>
    Источник примера (<a href="https://lollipopchainsaw.fandom.com/wiki/Nick_Carlyle">https://lollipopchainsaw.fandom.com/wiki/Nick_Carlyle</a>).
  </em>
</p>


### Задача S... ()


## Картинки на выставку