## Введение

Turtle Graphics — это популярная библиотека в Python, которая предоставляет простой и интуитивно понятный способ создания графики с помощью команд, напоминающих рисование черепашкой. Эта библиотека идеально подходит для начинающих программистов, так как позволяет визуализировать программные концепции и развивать навыки программирования в увлекательной форме.

В данном коспекте мы рассмотрим, как с помощью библиотеки Turtle можно создать круг. Мы изучим основные команды, необходимые для работы с графикой, и разберем, как управлять черепашкой для рисования различных фигур. Создание круга — это отличный способ понять основы работы с координатами и углами, а также научиться использовать циклы и функции для упрощения кода.

В процессе работы мы напишем простой код, который будет рисовать круг, и проанализируем его шаг за шагом. Это поможет вам не только освоить библиотеку Turtle, но и развить логическое мышление и навыки решения задач. Давайте начнем наше путешествие в мир графики на Python!

# Импорт библиотек и файлов
В начале файла импортируются модули `draw`, `ball` и `anim`, откуда берутся необходимые классы и функции для работы программы.

# Функция Main
Функция `Main` имеет единую ответственность — служит точкой входа в программу и вызывает основной функционал.

- Создается объект `BB` класса `Ball` с параметрами: координаты (x=0, y=0) и радиусом 15.
- Создается объект класса `Anim`, которому передаются:
  - параметр FPS (кадры в секунду) = 60,
  - объект класса `Draw`,
  - и объект `Ball` для анимации.
- Вызывается метод `anim` объекта `Anim` с объектом `BB` для запуска анимации.

# Запуск программы
Функция `Main` вызывается вне определения, что запускает всю вышеописанную логику.

---

Данный код организует структуру программы, разделяя создание объектов и вызов анимации через удобную точку входа `Main`.

# Класс Draw — управление черепашкой для рисования

Импортируется библиотека `turtle`. Класс `Draw` отвечает за визуализацию объектов с помощью черепашки.

## Конструктор `__init__`
- Создается объект черепашки `self.t`.
- Черепашка скрывается (`hideturtle`), чтобы не мешать при рисовании.
- Получается объект экрана `self.screen`.
- Управление обновлением экрана отключается (`tracer(0)`) для оптимизации отрисовки.

## Метод `teleport(self, x, y)`
- Поднимает перо (`penup`) — чтобы не рисовать линию при перемещении.
- Перемещает черепашку в координаты (x, y).
- Опускает перо (`pendown`) для дальнейшего рисования.

## Метод `circle(self, ball)`
- Использует метод `teleport` для перехода к координатам объекта `ball`.
- Рисует круг с радиусом `ball.radius` в точке (ball.x, ball.y) с помощью `turtle.circle`.

---

Данный класс обеспечивает низкоуровневую работу с черепашкой для удобного рисования объектов с заданными координатами и размерами.

# Класс Ball — модель шара

Класс `Ball` описывает объект шара с его позицией и размером.

## Конструктор `__init__`
- Принимает параметры:
  - `x` — координата по оси X,
  - `y` — координата по оси Y,
  - `radius` — радиус шара.
- Сохраняет эти параметры в свойства объекта:
  - `self.x`, `self.y`, `self.radius`.
- В коде закомментирована возможная переменная `speed` для дальнейшего расширения.

---

`Ball` служит простой структурой данных для представления круга с определённой позицией и размером.

# Класс Anim — анимация объектов

Класс `Anim` отвечает за анимацию объектов на экране с заданной частотой кадров (FPS).

## Конструктор `__init__`
- Принимает параметры:
  - `fps` — количество кадров в секунду,
  - `draw` — объект класса `Draw`.
- Вычисляет интервал обновления экрана как `1 / fps` и сохраняет его в `self.interval`.
- Инициализирует таймер `self.time` с текущим временем.
- Сохраняет объект `draw` для дальнейшего использования.

## Метод `anim(self, ball)`
- Запускает бесконечный цикл для анимации.
- Вычисляет время, прошедшее с последнего обновления (`elapsed_time`).
- Если время меньше интервала, программа приостанавливается на оставшееся время (`time.sleep`).
- Печатает радиус шара (`print(ball.radius)`).
- Вызывает метод `circle` объекта `draw` для рисования шара.
- Обновляет экран с помощью `self.draw.screen.update()`.

---

Класс `Anim` обеспечивает управление анимацией объектов, позволяя обновлять их положение и визуализацию на экране с заданной частотой.


```python
graph TD
    subgraph Основной поток программы
        Start(Start) -->|Создать объект класса Draw| DrawObj((Draw))
        Start -->|Создать объект класса Ball| BallObj((Ball))
        Start -->|Создать объект класса Anim| AnimObj((Anim))
        AnimObj -- Анимация шара --> BallObj
        AnimObj -- Отрисовка --> DrawObj
    end

    subgraph Класс Draw
        DrawObj -- Перемещение перьевого инструмента --> Teleport[x,y]
        DrawObj -- Рисовать круг --> Circle(radius)
    end

    subgraph Класс Ball
        BallObj -- Координата X --> X
        BallObj -- Координата Y --> Y
        BallObj -- Радиус --> R
    end

    subgraph Класс Anim
        AnimObj -- FPS --> Fps
        AnimObj -- Интервал обновления --> Interval
        AnimObj -- Время начала --> TimeStart
        AnimObj -- Экран обновления --> ScreenUpdate
    end
    ```