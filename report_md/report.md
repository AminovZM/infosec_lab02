---
# Front matter
title: "Отчёт по лабораторной работе №2"
subtitle: "Дискреционное разграничение прав в Linux. Основные атрибуты"
author: "Аминов Зулфикор Мирзокаримович"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Misc options
indent: true
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

Получение практических навыков работы в консоли с атрибутами фай-
лов, закрепление теоретических основ дискреционного разграничения до-
ступа в современных системах с открытым кодом на базе ОС Linux.

# Выполнение работы

## Создание учетной записи пользователя

Создали учетной запись пользователя guest, установил парол и вошел в нее.

## Определили директорию, в которой мы находились, командой pwd

![Определение директорию](image/1.png){ #fig:001 width=100% height=100% }

## Уточнили имя нашего пользователя

![Уточнение имя пользователя](image/2.png){ #fig:002 width=100% height=100% }

## Уточнили имя нашего пользователя, его группу, а также группы, куда входит пользователь, командой id

![Команда id](image/3.png){ #fig:003 width=100% height=100% }

## Сравнили вывод id с выводом команды groups.

![Команда groups](image/4.png){ #fig:004 width=100% height=100% }

## Просмотрели файл /etc/passwd командой cat /etc/passwd

![Файл /etc/passwd](image/5.png){ #fig:005 width=100% height=100% }

## Также просмотрели файл /etc/passwd командой cat /etc/passwd | grep guest

![cat /etc/passwd | grep guest](image/6.png){ #fig:006 width=100% height=100% }

## Определили существующие в системе директории командой ls -l /home/

![Определение существующие в системе директории](image/7.png){ #fig:007 width=100% height=100% }

## Создали в домашней директории поддиректорию dir1 командой mkdir dir1

Определили командами ls -l и lsattr, права доступа и расширенные атрибуты

## Снимали с директории dir1 все атрибуты командой chmod 000 dir1

![Снятие атрибуты](image/8.png){ #fig:008 width=100% height=100% }

## Проверили правильность выполнения команды ls -l

![Проверка правилность](image/9.png){ #fig:009 width=100% height=100% }

## Созданые в директории dir1 файл file1 командой echo "test" > /home/guest/dir1/file1

Не удалось создать файл file1

## Заполнили таблицу

![Заполнение таблиц](image/10.png){ #fig:010 width=100% height=100% }

# Выводы

Получили практических навыков работы в консоли с атрибутами фай-
лов, закрепление теоретических основ дискреционного разграничения до-
ступа в современных системах с открытым кодом на базе ОС Linux.
