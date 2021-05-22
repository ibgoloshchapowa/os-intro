---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе №10"
subtitle: "Текстовой редактор emacs"
author: "Голощапова Ирина Борисовна"

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

Ознакомиться с операционной системой Linux. Получить практические навыки работы с редактором Emacs.

# Библиография
[Работа в редакторе vi. Особенности использования](https://docs.altlinux.org/ru-RU/archive/2.3/html-single/junior/alt-docs-extras-linuxnovice/ch02s10.html)


[Vi - Википедия](https://ru.wikipedia.org/wiki/Vi)



[Полная справка по редактору vi](https://remoteshaman.com/unix/common/polnaya-reference-at-vi-redaktoru)


# Выполнение лабораторной работы


 ### Задание 1. "Создание нового файла с использованием vi"

1. Создала каталог с именем ~/work/os/lab09.

![каталог lab09](screen/1.1.png){ #fig:001 width=70% } 

***Рис.1 "каталог lab09"*** 

2. Перешла во вновь созданный каталог, вызвала редактор vi и создала файл hello.sh
```vi hello.sh```

![файл hello.sh](screen/1.2.png){ #fig:001 width=70% }

***Рис.2 "файл hello.sh"***

3. Нажала клавишу i и ввела следующий текст.
```#!/bin/bash
HELL=Hello
function hello {
LOCAL HELLO=World
echo $HELLO
}
echo $HELLO
hello
```

![редактирование файла hello.sh](screen/1.4.png){ #fig:001 width=70% }

***Рис.3 "редактирование файла hello.sh"***

5. Нажала клавишу ```Esc``` (для перехода в командный режим после завершения ввода
текста). Нажала ```:``` для перехода в режим последней строки и внизу экрана
появилось приглашение в виде двоеточия. Нажала ```w``` (записать) и ```q``` (выйти), а затем клавишу ```Enter``` для сохранения текста и завершения работы.


![сохранение и выход из файла hello.sh](screen/1.5-7.png){ #fig:001 width=70% }

***Рис.4 "сохранение и выход из файла hello.sh"***

8. Сделала файл исполняемым

![исполняемый файл hello.sh](screen/1.8.png){ #fig:001 width=70% }

***Рис.5 "исполняемый файл hello.sh"***

### Задание 2. "Редактирование существующего файла"
1. Вызвала vi на редактирование файла
```vi ~/work/os/lab06/hello.sh```

![вызов файла hello.sh на редактирование](screen/2.1.png){ #fig:001 width=70% }

***Рис.6 "вызов файла hello.sh на редактирование"***


2. Установила курсор в конец слова HELL второй строки.

![курсор в начале слова HELL](screen/2.1.png){ #fig:001 width=70% }

***Рис.7 "курсор в начале слова HELL"***

3. Перешла в режим вставки и заменила на HELLO. Нажала Esc для возврата в
командный режим.

![замена HELL на HELLO](screen/2.3.png){ #fig:001 width=70% }

***Рис.8 "замена HELL на HELLO"***

4. Установила курсор на четвертую строку и стерла слово LOCAL.

![удаление слова LOCAL](screen/2.4.png){ #fig:001 width=70% }

***Рис.9 "удаление слова LOCAL"***

5. Перешла в режим вставки и набрала следующий текст: ```local```, нажала ```Esc```
для возврата в командный режим.

![ввод local](screen/2.5.png){ #fig:001 width=70% }

***Рис.10 "ввод local"***

6. Установила курсор на последней строке файла. Вставила после неё строку, содержащую следующий текст: ```echo $HELLO```.

![echo $HELLO](screen/2.6.png){ #fig:001 width=70% }

***Рис.11 "echo $HELLO"***

7. Нажала ```Esc``` для перехода в командный режим. Удалила последнюю строку.

![удаление последнем строки](screen/2.7-8.png){ #fig:001 width=70% }

***Рис.12 "удаление последнем строки"***

9. Ввела команду отмены изменений ```u``` для отмены последней команды.

![отмена последних изменений](screen/2.9.png){ #fig:001 width=70% }

***Рис.13 "отмена последних изменений"***

10. Ввела символ ```:``` для перехода в режим последней строки. Записала произведённые изменения и выйдите из vi.

![сохранение и выход из редактора vi](screen/2.10.png){ #fig:001 width=70% }

***Рис.14 "сохранение и выход из редактора vi"***



# Выводы

В ходе лабораторной работы я ознакомилась с операционной системой Linux. Получила практические навыки работы с редактором Emacs.





# Контрольные вопросы


