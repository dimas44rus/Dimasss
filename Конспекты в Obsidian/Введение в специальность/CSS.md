#css #css-basics #css-selectors #css-properties #css-values #css-layout #css-grid 
#css-flexbox #css-media-queries #css-preprocessors #css-frameworks
1. Определение
2.  Цели
3. Синтаксис
4. Типы CSS



## 1. Определение
CSS (Cascading Style Sheets) - это формальный язык декодирования и описания внешнего вида документа, то есть он отвечает за то, как выглядят веб-страницы: цвет фона и декоративных элементов, размер и стиль шрифтов. CSS взаимодействует с другим языком разметки - HTML, который отвечает за размещение элементов на странице.

CSS - это язык таблицы стилей. Это означает, что он позволяет применять стили выборочно к элементам в документах HTML.
## 2. Цели CSS (Cascading Style Sheets) можно сформулировать следующим образом:

**Основные цели CSS:**

1. **Улучшение внешнего вида веб-страницы**: CSS позволяет разработчикам контролировать внешний вид веб-страницы, включая цвет, шрифт, размер, стиль и другие аспекты дизайна.
2. **Упрощение кода HTML**: CSS позволяет отделить презентационную логику от структуры HTML, что упрощает код и делает его более易ным для поддержки.
3. **Увеличение доступности**: CSS
4. **Улучшение пользовательского опыта**: CSS может помочь создать более привлекательный и интерактивный пользовательский интерфейс, что улучшает общ

**Дополнительные цели CSS:**

1. **Сокращение времени разработки**: CSS позволяет разработчикам быстро и эффективно создавать и изменять стили веб-страниц.
2. **Повышение гибкости**: CSS позволяет легко изменять внешний вид веб-страницы в зависимости от различных факторов, таких как устройство, браузер или язык.
3. **Улучшение производительности**: CSS может помочь ускорить загрузку
4. **Сокращение количества кода**: CSS может помочь уменьшить количество кода, необходимого для

В целом, цели CSS заключаются в том, чтобы создать более привлекательный, доступный и интерактивный пользовательский интерфейс, упрощая при этом процесс разработки и поддержки веб-страниц.
## 3. Синтаксис
Синтаксис CSS (Cascading Style Sheets) состоит из следующих элементов:

### Селекторы (Selectors)

Селекторы используются для выбора элементов HTML, к которым будет применяться стиль. Селекторы могут быть следующих типов:

- **Тег** (Tag): выбирает элементы по имени тега, например, `p` или `div`.
- **Класс** (Class): выбирает элементы по имени класса, например, `.big` или `.header`.
- **Идентификатор** (ID): выбирает элементы по уникальному идентификатору, например, `#header` или `#footer`.
- **Атрибут** (Attribute): выбирает элементы по наличию или значению атрибута, например, `[hreflang="en"]` или `[type="text"]`.
- **Комбинатор** (Combinator): выбирает элементы по их отношениям с другими элементами, например, `div > p` или `ul + li`.

### Свойства (Properties)

Свойства CSS определяют стиль элементов, выбранных селектором. Свойства состоят из имени свойства и значения, разделенных двоеточием, например, `color: red;` или `font-size: 18px;`.

### Значения (Values)

Значения CSS определяют конкретное значение свойства, например, `red`, `18px`, или `bold`.

### Объявления (Declarations)

Объявления CSS состоят из селектора, свойства и значения, разделенных двоеточием, например, `p { color: red; }` или `div { background-color: silver; }`

## 4. Типы CSS
1. **Inline CSS** - стиль, добавленный непосредственно в тег HTML.
2. **Internal CSS** - стиль, добавленный в тег `<style>` внутри HTML-документа.
3. **External CSS** - стиль, хранящийся в отдельном файле с расширением `.css` и подключаемый к HTML-документу.
4. **Embedded CSS** - стиль, добавленный в тег `<style>` внутри HTML-документа, но с помощью атрибута `scoped`.
5. **Preprocessor CSS** - стиль, написанный с помощью препроцессора, такого как Sass или Less, и компилируемый в обычный CSS.
6. **PostCSS** - инструмент, позволяющий писать CSS с использованием будущих функций CSS, а затем компилирующий его в обычный CSS.
7. **CSS Frameworks** - готовые библиотеки CSS, предоставляющие готовые стили и компоненты для быстрого создания веб-приложений.
8. **CSS Grid** - тип CSS, используемый для создания сложных сеток и макетов на веб-страницах.
9. **CSS Flexbox** - тип CSS, используемый для создания гибких и адаптивных макетов на веб-страницах.

#### Чем отличается  от HTML?
CSS (Cascading Style Sheets) и HTML (HyperText Markup Language) - это два языка, используемых для создания веб-страниц. Они имеют разные цели и функции, но работают вместе, чтобы создать полноценный веб-сайт.

**HTML**

HTML - это язык разметки, используемый для создания структуры и содержимого веб-страницы. Он определяет, какие элементы будут отображаться на странице, такие как заголовки, параграфы, изображения, ссылки и т.д. HTML состоит из тегов, которые окружают содержимое и определяют его тип.

**CSS**

CSS - это язык стиля, используемый для описания внешнего вида и форматирования веб-страницы. Он определяет, как будут отображаться элементы HTML, такие как цвет, шрифт, размер, стиль и т.д. CSS позволяет отделить презентационную логику от структуры HTML, что упрощает код и делает его более易ным для поддержки.

**Основные отличия**

1. **Цель**: HTML используется для создания структуры и содержимого веб-страницы, а CSS - для описания внешнего вида и форматирования.
2. **Синтаксис**: HTML использует теги для определения элементов, а CSS использует селекторы, свойства и значения для описания стиля.
3. **Функции**: HTML определяет, какие элементы будут отображаться на странице, а CSS определяет, как они будут отображаться.
4. **Взаимодействие**: HTML и CSS работают вместе, чтобы создать полноценный веб-сайт. HTML предоставляет структуру и содержимое, а CSS - внешний вид и форматирование.

В целом, HTML и CSS - это два языка, которые дополняют друг друга и используются для создания веб-страниц. HTML создает структуру и содержимое, а CSS - внешний вид и форматирование.
