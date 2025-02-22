---
## Front matter
title: "Oтчёта по лабораторной работе №1"
subtitle: "Простейший вариант"
author: "Дмитрий Сергеевич Кулябов"

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

Целью данной работы является приобретение практических навыков
установки операционной системы на виртуальную машину, настройки ми-
нимально необходимых для дальнейшей работы сервисов

# Задание

утсановить Rocky linux.

# Выполнение лабораторной работы


сначала я настройл и выбрал основные опции виртуальной машины. (рис. [-@fig:001		]).

![название и .iso](image/01.jpg){#fig:001		 width=70%}


Потом я выбрал объем оперативной памяти и количество ядер процессора (рис. [-@fig:002		]).

![оперативная память и ядра процессора](image/02.jpg){#fig:002		 width=70%}

Дальше настроил объем жесткого диска(в этом случае я выбрал 100 гб)  (рис. [-@fig:003		]).

![жесткий диск](image/03.jpg){#fig:003		 width=70%}

После того как я настроил характеристики виртуальной машины,я изменил устройство указатели на tablet usb и потом я запутил ВМ (рис. [-@fig:004		]) (рис. [-@fig:005		]).



![завершить настройки ВМ](image/04.jpg){#fig:004		 width=70%}

![настройка устройства указатели ](image/05.jpg){#fig:005		 width=70%}


После того как я запустил ВМ я смог выбрать начать уставоку ОС  (рис. [-@fig:006		]).

![установка ОС](image/06.jpg){#fig:006		 width=70%}

Потом я выбрал язык машины, в моем случае я выбрал англиский язык (рис. [-@fig:007		]).

![выбор языка](image/07.jpg){#fig:007		 width=70%}


Потом я выбрал какой жесткий диск машина будет использовать (рис. [-@fig:008		]).


![жесткий диск](image/08.jpg){#fig:008		 width=70%}

Дальше я выбрал установку программное обеспечение "development tools" (рис. [-@fig:009		]).

![development tools](image/09.jpg){#fig:009		 width=70%}

Потом я отключил KDUMP  (рис. [-@fig:010		]).

![KDUMP](image/10.jpg){#fig:010		 width=70%}

Затем я изменил название хоста на qjarishekka (рис. [-@fig:011		]).
 

![название хоста](image/11.jpg){#fig:011		 width=70%}


Потом я указал пароль root (рис. [-@fig:012		]).

![пароль root](image/12.jpg){#fig:012		 width=70%}

Дальше я настроил пользователя  (рис. [-@fig:013		]).

![пользователь](image/13.jpg){#fig:013		 width=70%}

После того как я настроил все опции я начал установку ОС (рис. [-@fig:014		]).

![установка](image/14.jpg){#fig:014		 width=70%}

Когда установка совершена я перегрузил систему (рис. [-@fig:015		]).

![перезагрузка](image/15.jpg){#fig:015		 width=70%}

Потом я входил в систему используя пользователя которого я настроил и открыл терминал чтобы искать основные информацию (рис. [-@fig:016		]).

![терминал](image/16.jpg){#fig:016		 width=70%}

Потом я выполнил некоторые команды чтобы получить информацию о системе (рис. [-@fig:017 - рис. [-@fig:022		]).

![основная информация](image/17.jpg){#fig:017	 width=70%}

![основная информация](image/18.jpg){#fig:018		 width=70%}

![основная информация](image/19.jpg){#fig:019		 width=70%}

![основная информация](image/20.jpg){#fig:020		 width=70%}

![основная информация](image/21.jpg){#fig:021		 width=70%}

![основная информация](image/22.jpg){#fig:022		 width=70%}



# Выводы

в эту лабораторную работу я смог установить ОС Rocky linux чтобы работать с ней.

# Список литературы{.unnumbered}

::: {#refs}
:::
