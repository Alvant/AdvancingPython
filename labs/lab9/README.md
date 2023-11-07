# Lab 9: ООП и пушка 2

Лаба: http://cs.mipt.ru/python/lessons/lab9.html.






## Задача (Пирог)

Зима — это время борьбы за жизнь.
По крайней мере, так считает Маша.
Да, казалось бы, при чём тут зима, ведь ещё ноябрь.
Однако не так давно уже были заморозки, под ногами каток, перемежающийся оазисами из относительно глубоких ещё непромёрзших луж, а с неба падал "дождеснег"...

Но Маша не хочет поддаваться "мрачным" мыслям!
Чтобы немного поднять настроение и себе, и коллегам по учёбе, Маша решила испечь яблочный пирог.
У неё есть рецепт, для которого надо будет купить продукты, и есть несколько магазинов в окрестности.
Помогите Маше: напишите программу, с помощью которой она могла бы сразу понять, сможет или нет купить в магазинах все необходимые ингредиенты, и если сможет, то в каком именно магазине (Маша бы хотела купить всё в одном месте) и на какую сумму выйдет вся покупка (хотя что такое деньги, когда речь идёт о том, чтобы немного скрасить будни).

Рецепт описан в файле [recipe.txt](./files/apple\_pie/recipe.txt): состав по пунктам и описание последовательности действий.
Информация о магазинах приведена в файле [shops.txt](./files/apple\_pie/shops.txt) в следующем формате: название магазина, расстояние до него от дома Маши, и далее раздел о продуктах в этом магазине.
Для каждого продукта известны: название, единица измерения (строка; штука, килограмм и т.п.), количество единиц в одной упаковке (флотовое число; предлагается считать, что фрукты тоже продаются в "упаковке" по одной штуке, то есть для фруктов известна как бы "средняя цена" за одну штуку, а не за килограмм), цена за упаковку в рублях (флотовое число), а также количество упаковок в наличии в описываемом магазине (целое число).

В программе должны использоваться классы Рецепта и Магазина.
Обход магазинов надо начинать в порядке от ближайшего в дальнему (если в ближнем уже можно купить все нужные для рецепта продукты, пусть и, возможно, по большой цене, то дальше не идём).
Как только найдет магазин, где можно всё купить, программа завершается и выводит ответ.
Если же окажется так, что ни в одном магазине нельзя купить всего необходимого, то... но, нет, такого точно не будет -- Маша обязательно всё купит и испечёт пирог!


## Задача (Снеговик)

Что нужно, чтобы слепить снеговика?
Основное -- это желание и готовность некоторое время позаниматься ерундой.
И, конечно, нужен снег.
Много снега.
Не рыхлого, но немного влажного, который легко лепить.
Далее, нужно скатать несколько комьев разного размера, и в нужном порядке нанизать один на другой (маленький на большой).
После этого снеговик можно считать в целом готовым (детали в виде веточек, морковки и ведра оставим за кадром).

Напишите программу -- исполнитель, который лепит снеговика.
Программа должна распознавать две команды:
* `катать` -- скатывает текущий ком снега, в результате его радиус увеличивается (на 2 см, если ком уже катали; если же он новый и ещё не начат, то сразу на 10 см)
* `положить` -- кладёт текущий ком снега на уже начатого снеговика, если последний положенный ком был больше размером; в противном случае -- ком ложится в основание нового снеговика и далее программа будет лепить его

Например:
```
# Снеговик из одного кома радиусом 10 + 2 = 12 см
катать
катать
положить


# Снеговик из двух комов: радиусом 12 см в основании и 10 см повыше
катать
катать
положить
катать
положить

# Два снеговика, первый из одного кома радиусом 10 см, второй из кома радиусом 12 см
катать
положить
катать
катать
положить
```

В файле [snowman.txt](./files/snowman/snowman.txt) описана последовательность действий, которая подаётся на вход исполнителю (в первой строчке указано общее число действий `n`, далее в `n` строках идут сами действия).
Выведите на экран количество слепленных снеговиков, высоту самого высокого снеговика, ширину самого широкого, и максимальное количество комьев в одном снеговике.

Как часть решения задачи предлагается реализовать классы: СнежныйКом, Снеговик и Исполнитель.
Ком характеризуется радиусом, снеговик -- составляющими его комьями (при этом важен порядок).
Исполнитель должен уметь совершать описанные действия: скатать ком и положить его на снеговика.






## Задача (Букет)

Как-то вечером в цветочный магазин пришёл посетитель.
Со вполне определённым запросом: он бы хотел составить букет из семи фиолетовых цветов одного вида, причём так, чтоб хотя бы пять из семи цветов были ещё не до конца распустившимися.
Напишите программу, которая бы помогла флористу быстро понять, получится ли удовлетворить такой запрос (или лучше немного расспросить посетителя и попытаться предложить ему что-нибудь ещё).
Если описанный букет составить можно (цветы есть в наличии), то надо вывести на экран общую стоимость.
Если же букета составить нельзя, программа должна вывести на экран максимальное нечётное число ещё нераспустившихся фиолетовых цветов одного вида.

Информация об имеющихся в цветочном магазине цветах приведена в файле [flowers.txt](./files/flowers/flowers.txt): для каждого цветка известно название (строка; роза, тюльпан и т.п.), цвет (строка), полностью ли распустился (булевское значение), и цена в рублях (целое число).

Помимо того, чтоб просто помочь флористу и посетителю магазина составить букет, программа также должна использовать "силу ООП".
Предлагается реализовать два класса: Цветок и Букет.
У цветка должны быть все описанные свойства, букет же характеризуется просто составляющими его цветами.
Объекты цветов предлагается "научить" складываться через `+` и умножаться на число, при этом получается букет:
```python
flower1 + flower2 + flower3  # букет из цветов flower1, flower2, flower3
flower * 3                   # букет из цветов flower, flower, flower
```
А букет предлагается научить красиво печататься в принте: результат принта для букета -- символ `⚘`, повторённый столько раз, сколько всего есть цветов в букете:
```python
bouquet = flower1 + flower2 + flower3

print(bouquet)  # ⚘⚘⚘
```


## Задача (Pac-Man)

Предлагается с помощью ООП и `pygame` реализовать игру типа [Пакмана](https://ru.wikipedia.org/wiki/Pac-Man).
Можно сделать что-то совсем базовое в плане "геймплея", главное -- чтобы было несколько взаимодействующих друг с другом классов (и чтобы всё-таки было играбельно).

Например, пусть есть один "активный кругляш" (Пакман), которым игрок может управлять с помощью стрелок клавиатуры (влево, вправо, вверх, вниз).
И пусть на поле в случайном месте иногда появляется "статичный кругляш", который надо съесть (при этом съеденный кругляш пропадает с поля, а Пакман, например, увеличивается в размере).

(Описанный вариант игры -- это даже, может, больше <a href="https://en.wikipedia.org/wiki/Snake_(video_game_genre)">Змейка</a>, а не Пакман, но не важно 🙂)



## Задача* (Шахматы)

Напишите программу -- генератор игры в шахматы.
Игра начинается со стандартной расстановки (поле 8 x 8, есть чёрные и белые фигуры, с каждой стороны 8 пешек, 2 ладьи, 2 коня, 2 слона, король и королева).
Далее "игроки" начинают совершать случайные (но при этом корректные) ходы.
То есть обычный ход игрока заключается в случайном выборе фигуры (из тех, что могут сделать ход) и в совершении случайного (но допустимого) хода за выбранную фигуру.
Ходом может быть либо просто перемещение своей фигуры по полю, либо "съедание" при этом фигуры противника, либо объявление шаха (в качестве более простого варианта игры предлагается такой, в котором на шах можно "не обращать внимания" и когда игра заканчивается просто случайным "съеданием" короля; в качестве более полного варианты игры стоит учесть и ситуацию с шахом: надо обязательно защитить короля -- и такая игра уже должна заканчиваться матом или патом).

Предлагается реализовать классы для всех шахматных фигур и, возможно, ещё некоторые другие, если будет иметь смысл (класс для поля? класс для игрока?).

В качестве выхода программа должна записать в текстовый файл в первой строчке имя победителя ("чёрные" или "белые") и далее построчно последовательность совершённых в процессе игры ходов в шахматной нотации.


## Задача* (Сквозь снег)

День рождения Маши зимой, в конце декабря.
И вчера вечером, перед сном, она подумала об авторе <a href="../lab5/README.md#задача-6-послание">послания</a>: знает ли он, когда у неё день рождения? готовится ли что-то сделать для неё в этот день? что-то подарить или, может, даже "раскрыться", перестать быть анонимом?..

С этими мыслями Маша и заснула, и ей приснился следующий сон.

Сегодня её день рождения.
Уже поздний вечер, на улице темно, горят фонари, дует ветер, идёт сильный снег, а "её аноним" бежит по улицам с букетом цветов, чтобы успеть до конца дня вручить ей.
Он примерно знает, где она живёт, но ещё никогда в том районе не был, поэтому точной дороги не знает и бежит "полунаугад", скорее веря, чем точно зная, что придёт куда нужно, к дому Маши.
А тут ещё и снег летит в лицо, в глаза, видимость плохая, и порой он начинает сомневаться, успеет ли вовремя...

Напишите с помощью ООП и `pygame` следующую игру по мотивам сна Маши.
Есть поле со стенками: вертикальными и горизонтальными.
Через верхнюю границу поля по всей длине сверху вниз летят "снежинки" (маленькие шарики).
Они пролетают всё поле, но сквозь горизонтальные стенки не проходят.
Игрок управляет "активным кругляшом" размера больше снежинок, который в начале игры стоит перед горизонтальной стенкой.
Управление (перемещение кругляша) осуществляется стрелками клавиатуры (влево, вправо, вверх, вниз).
У игрока есть "букет" (несколько цветов, например семь).
Ещё на поле есть "дом": это выделенная клетка поля, куда должен добраться игрок (принести букет).
Сложность в том, что надо стараться избегать столкновений со снежинками.
Три "пойманные" снежинки приводят к следующему: "замерзает" один цветок букета, а игроку снег "застилает глаза" и он теряет ориентацию в пространстве.
Потеря ориентации выражается в том, что дом "перемещается": исчезает со старого места и оказывается на новом, далеко от игрока.
Игра заканчивается, если персонаж добирается до дома с хотя бы одним цветком в запасе, или если все цветы замерзают (а персонаж окончательно теряет дорогу и так и остаётся блуждать среди снежинок).

