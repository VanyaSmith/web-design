# О чём должен помнить веб-дизайнер

От технологов и программистов — веб-дизанейрам. О чём нужно помнить, чтобы называть себя веб-дизайнером.

Сверстать можно всё, что можно придумать и воплотить в макете. Вопрос только во времени, деньгах и удобстве (времени и стоимости) расширения.



## Общее

**Веб-дизайнер — это инженер**. Веб-дизайнер — это не рисовальщик, он не придумывает «как будет выглядеть», он придумывает «как сделать, чтобы проект лучше всего решал поставленные задачи». На западе нет разделения на дизайнеров и верстальщиков. Если Вы совсем не умеете верстать (не представляете как это работает), Вы — не веб-дизайнер.

**Технически недоработанный макет осложняет работу технолога**. Для студий — это увеличение сроков разработки. Для фриланса — ухудшение кармы дизайнера в момент, когда технолог описывает клиенту список технических недоработок и/или неучтённых дизайнером ограничений.



## Макеты

**Макет нужно делать в sRGB**. Критично, обязательно. Иначе цвета в вёрстке могут отличаться от макетных.

**Макет должен иметь тот размер, в котором его нужно сверстать**. Размер(ы) выбирается, исходя из специфики проекта и целевой аудитории.

**В макетах допустим только режим наложения normal**. Критично, обязательно. И так будет, пока не [появится кроссбраузерная поддержка](http://caniuse.com/#search=blend) режимов наложения. Это не касается состоящих из множества иллюстраций, которые планируется соединять в одно изображение.

**Одна страница = один макет**. Обычно, это довольно объемные файлы, если хранить все на артбордах в едином файле, он будет подтормаживать.

**Скрытые слои не будут свёрстаны, если в ТЗ не указано иное**. Хотите показать, что в макете есть необходимые блоки, скрытые по умолчанию — приложите скриншоты в JPG, на которых эти слои видны. Обязательно складывайте нужные скрытые слои в отдельные папки и скрывайте такие папки.

**Оставляйте эффекты слоёв**. Эффекты, преобразованные в слои, ощутимо дольше верстать.



### Стайлгайд

**Должен быть стайлгайд**, в котором видны все необходимые состояния меняющихся элементов (интерактивных и просто настраиваемых) и типографическое оформление.

**Стайлгайд — это отдельный макет**. Это не текстовая инструкция как включать/выключать видимость слоёв, варианты композиции слоёв. Это не артборд, включённый в какой-либо макет.

**Для ссылок нужны состояния: «покой», «наведение», «клик» (последние два могут совпадать)**. Для навигационных ссылок нужно состояние «находимся на этой странице». Для контентных ссылок желательно состояние «ссылка посещалась».

**Для кнопок нужны состояния: «покой», «наведение», «клик», «блокирована»**. Иногда ещё нужно состояние «идёт процесс».

**Для текстовых полей форм нужны состояния: «покой», «получен фокус», «блокировано»**. Нет смысла прорисовывать состояние «клик».

**Для типографики нужно показать, как минимум, следующее**: заголовок 1, параграф, заголовок 2, параграф, заголовок 3, параграф, заголовок 4, параграф, параграф, маркированный список, параграф, нумерованный список, блочная цитата, параграф, таблица, параграф. Верстальщику важно увидеть все вертикальные расстояния (для этого и нужно чередование параграфами и два параграфа подряд).



## Модульные сетки

**Используйте модульные сетки**. Это сделает результат аккуратнее и, если не допускать глупых ошибок, ускорит реализацию макета в вёрстке. Самая глупая ошибка: создать модульную сетку, но не следовать ей.

**Модульные сетки — резиновые**. «Строку» с блоками модульной сетки можно вставить в блок любой ширины с сохранением параметров сетки. [Пример](http://getbootstrap.com/css/#grid-nesting).

**Граница ячеек модульной сетки — это середина промежутка между ячейками**. Блок не может выступать за середину этого промежутка — левая граница блока не может проходить по правой границе предыдущей ячейки модульной сетки.

**Идеал модульной сетки — 12 колонок**. Ибо 12 делится на 2, 3, 4 и 6. Чтобы придумывать свои (5-и, 8-колоночные) сетки нужно иметь действительно серьезные причины, ибо 8-колоночная сетка не позволит выстроить блоки по 3 в ряд.



## Текст, Шрифты

**Используйте легальные шрифты**. Есть множество хороших бесплатных. Например, на [Google Fonts](https://www.google.com/fonts).

**Используйте проверенные шрифты**. Перед использованием редкого шрифта или жирности проверяйте, как они отображаются во всех браузерах из ТЗ на всех операционных системах. Особенно в Windows и Linux, особенно кириллица. Самые «удачные» браузеры — IE (и Edge) и Firefox. За этим можно обратиться к технологу.

**Размеры шрифтов и интерлиньяж указывайте целыми числами в пикселях**. Браузер всё равно приведёт их к пиксельным размерам, пересчёт в другие единицы удобнее всего из пикселей.

**Выберите несколько размеров шрифта и придерживайтесь их**. Пример размеров: для заголовков 1, 2, 3 и 4 уровней, контентный, акцентированный (если не совпадает с каким-либо заголовочным), уменьшенный. Не плодите сущности без надобности.

**Вертикальные границы текстового блока проходят по границам «высоты линии», а не по границам букв первой и последней строк**.

**Избегайте менять кернинг и трекинг**. На подавляющем большинстве дисплеев очень мало «пикселей на дюйм», такое изменение нередко приводит к грустным эффектам: размытие символов, изменение их визуальной плотности.

**Интерлиньяж не должен быть меньше размера шрифта**. Всегда помните: если в текстовом блоке более одного слова, количество строк непредсказуемо. Не избегайте знакомства с «электрогардиографической одиннадцатиклассницей, псевдореволюцонизирующей циклопентанпергидрофенантрены».

**В вебе нет кроссбраузерных переносов**. Лучше не использовать переносы слов вообще. Расстановка символов мягкого переноса в тексте возможна (никто не будет делать это вручную, а автоматическое ещё нужно внедрить в проект), автоматический перенос в браузерах имеет [скромную поддержку](http://caniuse.com/#search=hyphens).



## Блоки

**ВСЕГДА думайте о переполнении блока текстом или другими блоками**. Почти для всех блоков нужно предусматривать возможность переполнения.

**У блоков есть внутренние и внешние отступы**. Внешние отступы пересекаются, а не суммируются.

**Однотипные блоки должны иметь однотипные свойства**. То есть, одинаковую ширину, высоту, цвет бордюра и пр.



## Векторная графика

**Используйте векторную графику**. Везде, где это возможно. При соблюдении некоторых условий, векторная графика технологичнее растровой, меньше размер файлов, поддерживает «эффекты внутри картинки», не требует ретинизации или ускоряет её.

**Создавайте векторную графику в векторных редакторах**. Для любых форм (сложнее прямоугольника со сглаженными краями или простых библиотечных форм) используйте [Adobe Illustrator](http://www.adobe.com/ru/products/illustrator.html) или [Inkscape](https://inkscape.org/ru/download/).

**Рисуйте векторные формы вместо работы кистью**. Заливки и формы, созданные кистью получаются «грязными» — имеют множество лишних ключевых точек, что крайне негативно сказывается на размере файла (иногда, оптимизировав количество точек, удавалось сжать SVG-изображение в 12 (!!!) раз — прим. Н.Г.).

**Предоставляйте векторную графику в том её размере, в котором она использована в макете**. Обязательно!

**Выравнивайте точки в кривых по пиксельной сетке**. Тогда иконки не будут мыльными на экранах с низким разрешением, к тому же будут лучше сжиматься. В редакторах настройка обычно называется «snap to pixel».

**Артборд должен быть подогнан по габаритам фигуры**. Для нескольких иконок одинакового размера допустимо, чтобы атрборды были одинаковых размеров (больше габарита фигур).

**Недопустимы режимы наложения, отличные от normal**. Кроссбраузерно это не сверстать.

**Всё, что может быть слито в единую форму, должно быть слито**. Это позволяет уменьшить размер файла (нередко, существенно).

**Удаляйте лишнее из векторных картинок**. Если какие-либо формы не видны, их нужно удалить, иначе они будут бессмысленно увеличивать размер файла.

**Избегайте наложения эффектов и трансформаций**. Переводите всё в кривые, применяйте трансформации.

**Избегайте градиентов и теней**. В некоторых случаях это может наложить ограничения на использование векторной графики.

**Для форм с заливкой не используйте обводку того же цвета, что и заливка**.



## Адаптивность

**Выберите 2-3 брейкпоинта и создавайте макеты для них**. Обычно, брейкпоинты следующие: 768, 992, 1200 пикс. (изредка добавляется ещё 480 пикс.). Традиционно, мы принимаем некую минимальную ширину (320 или 240), преобразования блоков происходят по достижении брейкпонта. Важно понимать: сделав макет в ширине 768, Вы показали то, как макет выглядит от 768 до следующего брекпоинта в большую сторону (скажем, 992).

**Уточняйте в ТЗ как ведет себя дизайн на разных брейкпоинтах**. По умолчанию, всё, что уже чем ≈1000 пикс. будет «резиновым».



## Разное

**Реализация нестандартных элементов форм увеличивает сроки проекта**. Особенно это касается нестандартных выпадающих списков (если не планируется использовать какое-либо готовое решение).

**Не рисуйте векторные иконки в [Sketch](http://bohemiancoding.com/sketch/)**. Такие иконки в 90% случаев технологически непригодны к использованию в векторном виде.



## Неприятные для технолога мелочи

**Отсутствие структуры слоёв**. Если слои не разложены по правильно именованным папкам, это несколько замедляет работу.

**Большие части макета в смарт-объектах**. «Шапка» и «подвал» в смарт-объектах не имеют смысла для экономии места, но увеличивают время доступа к своим составляющим. Это не относится к **связанным** смарт-объектам, в случае, когда макетов много.

**Изменение цвета объектов или текста при помощи прозрачности**. Плохо, т.к. технологически мы стараемся избегать прозрачности — много полупрозрачных объектов могут вызвать проблемы быстродействия страницы.

**Изменения вида векторных объектов эффектами Photoshop**. Это может привести к невозможности использования векторной графики.



# Об авторах

- [Николай Громов](http://nicothin.ru/contact). Технолог. Фрилансер. Преподаватель [EpicSkills](http://epixx.ru/) и [HTML Academy](https://htmlacademy.ru/). Первый сайт сделал в 2000 г.
- [Андрей Алексеев](https://github.com/aalexeev239). Технолог. Фрилансер.
