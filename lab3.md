---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе №3"
subtitle: "дисциплина: Информационная безопасность"
author: "Миличевич Александра"

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

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.
# Выполнение лабораторной работы

**Последовательность выполнения работы*

1. Так как у нас была учетная запись guest я создала guest1 и guest2 и добавила пароли
![Рис. 1.](image/p1.png){ #fig:001 width=70% }

2. Потом добавила guest2 в группу guest1.
![Рис. 2.](image/p2.png){ #fig:002 width=70% }

3. Осуществив вход в систему от двух пользователей на двух разных консолях: guest1 на первой консоли и guest2 на второй консоли.
 Для обоих пользователей командой pwd определила директорию, в которой  нахожусь. определила командами
groups guest1 и groups guest2, в какие группы входят пользователи guest1 и guest2. в guest1 входить guest2 так как мы добавили его там а guest2 не имеет подгруп.
![Рис. 3.](image/p3.png){ #fig:003 width=70% }

4. 
![Рис. 4.](image/p4.png){ #fig:004 width=70% }

5.Просмотрела файл командой cat /etc/group, все совпадает с информацией которую ранее видели.
![Рис. 5.](image/p5.png){ #fig:005 width=70% }

6. От имени пользователя guest2 выполнила регистрацию пользователя guest2 в группе guest командой
![Рис. 6.](image/p6.png){ #fig:006 width=70% }

7. От имени пользователя guest измените права директории /home/guest, разрешив все действия для пользователей группы: cразу после ээтого сняла их командой chmod 000 dir1
![Рис. 7.](image/p7.png){ #fig:007 width=70% }

8. 
![Рис. 8.](image/prava0.png){ #fig:008 width=70% }

9. 
![Рис. 9.](image/prava1.png){ #fig:008 width=70% }

10.различие в том что у группы даже с полными правами на директорию и на файл группа не может менять атрибуты файла.
![Рис. 10.](image/prava2.png){ #fig:008 width=70% }

11. определила те или иные минимально необходимые права для выполнения пользователем guest2 операций внутри директории dir1 и заполнила табл. “Минимальные права для совершения операций от имени пользователей, входящих в группу” 
![Рис. 11.](image/grupa.png){ #fig:008 width=70% }

# Выводы

Получила практические навыков работы в консоли с атрибутами файлов от имени груп.
