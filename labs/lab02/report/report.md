---
## Front matter
title: "Лабораторная работа №2"
subtitle: "Система контроля версий git"
author: "Чумаченко Оксана Алексеевна"

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

Изучить идеологию и применение средств контроля версий. Приобрести
практические навыки по работе с системой git.


# Задание

1) Изучить теорию
2) Настроить Гитхаб
3) Создать SSH ключ, а также рабочее пространство
4) Создание репозитория и настройка каталога курса
5) Выполнение заданий для самостоятельной работы

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

Создадим учетную запись на сайте https://github.com/ и заполним данные.
Сделаем предварительную конфигурацию git. Откроем терминал и введем следующие команды, указав имя и email владельца. 

![git](image/git.png){#fig:001 width=70%}

В пункте 2.4.3-2.4.4 требуется создать SSH ключ и рабочее простанство.

Создание SSH ключа:

![SSH](image/SSH_ключ.png){#fig:002 width=70%}

Создание публичного ключа:

![Создание публичного ключа](image/публичный_ключ.png){#fig:003 width=70%}

Создание каталога для предмета:

![Создание каталога для предмета](image/создание_каталога.png){#fig:004 width=70%}

В пунктах 2.4.5-2.4.6 требуется создать репозиторий курса и настроить
каталог курса.

Клонирование репозитория:

![Клонирование репозитория](image/клонирование.png){#fig:005 width=70%}

Перейдем в каталог курса и удалим лишние файлы:

![Удаление лишнего файла](image/удаление.png){#fig:006 width=70%}

Создаем необходимые каталоги и отправляем файлы на сервер:

![Команда make](image/команда_make.png){#fig:007 width=70%}

В пункте 2.5 требуется выполнить ряд самостоятельных заданий:

1) Создать отчет по выполнению лабораторной работы в соответствующим
каталоге рабочего пространства

2) Скопировать отчеты по выполнению предыдущих лабораторных работ в
соответствующие каталоги, созданного рабочего пространства

3) Загрузить файлы на гитхаб

![git add](image/git_add.png){#fig:008 width=70%}

![git push](image/git_push.png){#fig:009 width=70%}

# Выводы

Я изучила идеологию и применение средств контроля версий, и приобрела
навыки по работе с системой git.

# Список литературы{.unnumbered}

::: {#refs}
:::
