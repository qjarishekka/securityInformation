---
## Front matter
title: "отчёт по лабораторной работе №2"
subtitle: "Дискреционное разграничение прав в Linux. Основные атрибуты"
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

Получение практических навыков работы в консоли с атрибутами фай-
лов, закрепление теоретических основ дискреционного разграничения до-
ступа в современных системах с открытым кодом на базе ОС Linux1.

# Задание

Создать нового пользователя и смотреть его допуск 


# Выполнение лабораторной работы


Сначала я Создал новый пользователь  (рис. [-@fig:001		]).

		useradd guest

![Новый пользователь](image/01.png){#fig:001 	width=70%}

Потом я дал ему новый пароль  (рис. [-@fig:002		]).

		passwd guest

![новый пароль пользователя](image/02.jpg){#fig:002 	width=70%}

Дальше я вышел с системы и вшел еще раз используя новый пользователь (рис. [-@fig:101		]).


![вход в систему](image/101.png){#fig:101 	width=70%}


 
Потом я определил директорию, в которой я нашел (рис. [-@fig:003		]).

		pwd

![директория](image/03.png){#fig:003 	width=70%}

я смог смотреть что сейчас я был в каталоге /home/guest который принадлежал к пользователю guest и сейчас этот каталог является домашнем каталогом (рис. [-@fig:004		]).

		ls

![домашний каталог](image/04.png){#fig:004 	width=70%}


После этого, я определил кто настоящего пользователя (рис. [-@fig:005		]).

		whoami

![настоящий пользователь](image/05.png){#fig:005 	width=70%}


Потом я смотрел больше информацию о пользователе (рис. [-@fig:006		]).
		
		id

![информация о пользователе](image/06.png){#fig:006 	width=70%}

В моем случае, я uid пользователя - это 1001, gid - 1001, groups - 1001 

Потом я смотрел вывод команды groups (рис. [-@fig:007		]).

		groups

![команда groups](image/07.png){#fig:007 	width=70%}

вывод команды был guest который является названием группы, к которой принадлежит пользователь guest. они отличаются в тем, что команда id выводит в экран более информацию о пользователя и команда groups только выводит группу пользователя.

Потом я просмотрел файл /etc/passwd (рис. [-@fig:008		]).

		cat /etc/passwd 

![файл /etc/passwd](image/08.png){#fig:008 	width=70%}

В него находится, все пароли в машине. Потом чтобы быстро находить информацию о пользователе guest я использовал другую комнаду (рис. [-@fig:009		]).

		cat /etc/passed | grep guest

![grep](image/09.png){#fig:009 	width=70%}


Дальше я определил существующие в системе директории  (рис. [-@fig:010		]).

		ls -l /home/

![директории в системе](image/10.png){#fig:010 	width=70%}

к счастью я смог смотреть какие директории есть в системе.

Потом я использовал другую команду чтобы смотреть какие расширенные атрибуты установлены в директориях(рис. [-@fig:011		]).

		lsattr /home

![lsattr](image/11.png){#fig:011 	width=70%}

к сожалению, у меня не было доступа к инфорамации пользователя qjarishekka

Потом я создал каталог dir1 (рис. [-@fig:012		]).

		mkdir dir1

![новый каталог](image/12.png){#fig:012 	width=70%}

Потом я еще раз выполнил эти команды чтобы смотреть расширения и директории в системе (рис. [-@fig:013		]).

		ls -l 
		lsattr

![выполнение команд](image/13.png){#fig:013 	width=70%}


Затем я снял все атрибуты с директории dir1  (рис. [-@fig:014		]).

		chmod 000 dir1
		ls -l

![извлечение атрибутов](image/14.png){#fig:014 	width=70%}

Потом я попытался создать в каталоге dir1 новый файл file1 (рис. [-@fig:015		]).

		echo "test" > /home/guest/dir1/file1

![создание файла в каталоге dir1](image/15.png){#fig:015 	width=70%}

но я получил отказ потому что у этого каталога нет доступа для ничего 

Потом я хотел смотреть как эта ошибка отрохилась на создании файла но не смог смотреть потому что у меня не было доступа (рис. [-@fig:016		]).
		
		ls -l /home/guest/dir1

![сообщение о ошибок](image/16.png){#fig:016 	width=70%}

Потом я заполнил таблицу 


: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| права директории	|права файла	|создание файла	|удаление файла	|запись в файл	|чтение файла	|смена директории	|просмотр файлов в директории	|переименование файла	|смени атрибутов файла	|
|-----------------------|---------------|---------------|---------------|---------------|---------------|-----------------------|-------------------------------|-----------------------|-----------------------|
|000			|		|		|		|		|		|			|				|			|			|
|100			|		|		|		|		|		|			|				|			|			|
|200			|		|		|		|		|		|			|				|			|			|
|300			|		|		|		|		|		|			|				|			|			|
|400			|		|		|		|		|		|			|				|			|			|
|500			| 		|		|		|		|		|			|				|			|			|
|600			|		|		|		|		|		|			|				|			|			|
|700			|		|		|		|		|		|			|				|			|			|











# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::
