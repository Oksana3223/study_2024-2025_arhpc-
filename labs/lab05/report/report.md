---
## Front matter
title: "Отчет по лаборатрной работе №5"
subtitle: "Структура программы на языке ассемблера NASM. Системные вызовы в ОС GNU Linux"
author: "Оксана Алексеевна Чумаченко"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить структуру программы на языке ассемблера NASM.

# Задание

1. Создайте копию файла lab6-1.asm. Внесите изменения в программу (без использования внешнего файла in_out.asm), так чтобы она работала по следующему алгоритму: 
•вывести приглашение типа “Введите строку:”; 
•ввести строку с клавиатуры; 
•вывести введённую строку на экран

2. Получите исполняемый файл и проверьте его работу. На приглашение ввести строку введите свою фамилию.

3. Создайте копию файла lab6-2.asm. Исправьте текст программы с использование подпрограмм из внешнего файла in_out.asm, так чтобы она работала по следующему алгоритму: 
• вывести приглашение типа “Введите строку:”; 
• ввести строку с клавиатуры; 
• вывести введённую строку на экран.

4. Создайте исполняемый файл и проверьте его работу.

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

1. Открыть Midnight Commander

![Открыть МС](image/открыть_мс.png){#fig:001 width=70%}

2. Создать папку lab05 и внутри нее создать файл lab5-1.asm

![Создание папки lab05](image/Создание_папки.png){#fig:002 width=70%}

3. Открыть файл lab5-1.asm, ввести информацию из листинга 5.1 и сохранить изменения 

![Изменения текста](image/Изменения.png){#fig:003 width=70%}


4. Оттранслировать текст файла lab5-1.asm, выполнить компановку объектного файла и запустить файл

![Запуск файла](image/запуск_файла.png){#fig:004 width=70%}

5. Скачать и скопировать файл in_out.asm с помощью клавиши F5 

![Скомпанированный файл через F5](image/Скомпанированный_файл_F5.png){#fig:005 width=70%}

6. С помощью клавиши F6 скопировать файл lab5-1.asm с именем lab5-2.asm

![Скомпанированный файл через F6](image/Скомпанированный_F6.png){#fig:006 width=70%}

7. Исправить файл lab5-2.asm в соответствии с листингом 5.2 и заменить подпрограмму sprintLF на sprint 

![Изменения текста lab5-2.asm](image/изменения_lab5-2.png){#fig:007 width=70%}

8. Создать исполняемый файл и проверить его работу

![Создание и проверка файла](image/создание_файла.png){#fig:008 width=70%}

9. Создать копию файла lab5-1.asm и lab5-2.asm и внести изменения

![Создание копии файлов](image/Копирование.png){#fig:009 width=70%}

# Выводы

В процессе выполнения лабораторной работы я ознакомился со структурой программы на языке ассемблера NASM

# Список литературы{.unnumbered}

::: {#refs}
:::
