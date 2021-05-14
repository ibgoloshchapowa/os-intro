---
# Front matter
lang: ru-RU
title: "Лабораторная работа №8"
subtitle: "Командная оболочка Midnight Commander"
author: "Ирина Борисовна Голощапова"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Освоение основных возможностей командной оболочки Midnight Commander.
Приобретение навыков практической работы по просмотру каталогов и файлов; манипуляций с ними.


# Задание

Научиться работать в командной оболочке Midnight Commander.
Приобрести навыки работы во встроенном редакторе mc.

________
# Выполнение лабораторной работы
## Задания по mc:

1. Изучила информацию о mc, вызвав в командной строке man mc.

![man mc](screen/1.png){ #fig:001 width=70% }

2. Запустила из командной строки mc, изучила его структуру и меню.

![mc](screen/2.png){ #fig:001 width=70% }

3. Выполнила несколько операций в mc, используя управляющие клавиши
(операции с панелями; выделение/отмена выделения файлов, копирование/перемещение файлов, получение информации о размере и правах доступа
на файлы и/или каталоги и т.п.)

Операции с панелями:

![операции с панелями](screen/3.1.png){ #fig:001 width=70% }

Права доступа:

![права доступа](screen/3.2.png){ #fig:001 width=70% }

Копирование:

![копирование](screen/3.3.png){ #fig:001 width=70% }

Удаление:

![удаление](screen/3.4.png){ #fig:001 width=70% }

Перемещение:

![перемещение](screen/3.5.png){ #fig:001 width=70% }

Размер файлов и каталогов:

![размер файлов/каталогов](screen/3.6.png){ #fig:001 width=70% }

4. Выполнила основные команды меню левой (или правой) панели. Информация о файлах выводится довольно подробно.

Меню панели:

![меню панели](screen/4.1.png){ #fig:001 width=70% }

Информация о файле:

![информация о файле](screen/4.2.png){ #fig:001 width=70% }

Дерево:

![дерево](screen/4.3.png){ #fig:001 width=70% }

Формат списка файлов:

![формат списка файлов](screen/4.4.png){ #fig:001 width=70% }


5. Используя возможности подменю ```Файл``` , выполнила:

– просмотр содержимого текстового файла;

![содержимое файла](screen/5.2.png){ #fig:001 width=70% }

– редактирование содержимого текстового файла (без сохранения результатов
редактирования);

![редактирование](screen/5.3.png){ #fig:001 width=70% }

– создание каталога;

![создание каталога](screen/5.5.png){ #fig:001 width=70% }

– копирование в файлов в созданный каталог:

![копирование в созданный каталог](screen/5.6.png){ #fig:001 width=70% }

6. С помощью соответствующих средств подменю ```Команда``` осуществила:
– поиск в файловой системе файла с заданными условиями (например, файла
с расширением .c или .cpp, содержащего строку main);

![поиск](screen/6.1.png){ #fig:001 width=70% }

![результаты поиска](screen/6.2.png){ #fig:001 width=70% }

– выбор и повторение одной из предыдущих команд;

![history](screen/6.3.png){ #fig:001 width=70% }

– переход в домашний каталог;

![переход в домашний каталог](screen/6.4.png){ #fig:001 width=70% }

– анализ файла меню и файла расширений.

Файл расширений:

![файл расширений](screen/6.5.png){ #fig:001 width=70% }

Файл меню:

![файл меню](screen/6.6.png){ #fig:001 width=70% }


7. Вызвала подменю ```Настройки``` . Освоила операции, определяющие структуру
экрана mc (Full screen, Double Width, Show Hidden Files и т.д.)ю

![Структура экрана](screen/7.png){ #fig:001 width=70% }

__________________
## Задания по встроенному редактору mc:

1. Создала текстовой файл text.txt.

![файл text.txt](screen/11.png){ #fig:001 width=70% }

2. Открыла этот файл с помощью встроенного в mc редактора.

![открытие файла в mc](screen/22.png){ #fig:001 width=70% }

3. Вставила в открытый файл небольшой фрагмент текста.

![Структура экрана](screen/33.png){ #fig:001 width=70% }

4. Проделала с текстом следующие манипуляции, используя горячие клавиши:
4.1. Удалила строку текста при помощи клавиш ```Ctrl+y```

![Удаление строки](screen/44.1.png){ #fig:001 width=70% }

4.2. Выделила фрагмент текста и скопировала его на новую строку (```F5```).

![копирование фрагмента](screen/44.2.png){ #fig:001 width=70% }

4.3. Выделила фрагмент текста и перенесла его на новую строку(```F6```).

![перемещение фрагмента](screen/44.3.png){ #fig:001 width=70% }

4.4. Сохранила файл.

![сохранение файла](screen/44.4.png){ #fig:001 width=70% }

4.5. Отменила последнее действие с помощье сочетания клавиш ```Ctrl+u```

4.6. Перейшла в конец файла (нажав комбинацию клавиш ```Ctrl+x```) и написала некоторый текст.

![дополнение файла снизу](screen/44.5.png){ #fig:001 width=70% }

4.7. Перейшла в начало файла (нажав комбинацию клавиш ```Ctrl+z```) и написала некоторый текст.

![дополнение файла сверху](screen/44.6.png){ #fig:001 width=70% }

4.8. Сохранила и закрыла файл при помощи клавиши ```F10```.

5. Открыла файл с исходным текстом на некотором языке программирования (на языке С++)

![файл с++](screen/55.1.png){ #fig:001 width=70% }

6. Используя меню редактора, выключила подсветку синтаксиса (сочетание ```Ctrl+s```).

![подсветка синтаксиса](screen/55.2.png){ #fig:001 width=70% }


# Выводы

В ходе лабораторной работы я освоила основные возможности командной оболочки Midnight Commander.
Приобрела навыкы практической работы по просмотру каталогов и файлов; манипуляций с ними.

