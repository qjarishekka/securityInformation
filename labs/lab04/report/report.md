---
## Front matter
title: "Шаблон отчёта по лабораторной работе"
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

Получение практических навыков работы в консоли с расширенными атрибутами файлов

# Задание

выполнить все шаги лабораторной работы №4


# Выполнение лабораторной работы


Сначала я определил атрибуты файла /home/guest/dir1/file1 (рис. [-@fig:002		]).

		lsattr /home/guest/fir1/file1

![атрибуты файла file1](image/02.png){#fig:002 	width=70%}


Потом я установил права, разрешающие чтение и запись (рис. [-@fig:003		]).

		chmod 600 file1

![изменение прав доступа](image/03.png){#fig:003 	width=70%}


Потом я установил на файл file1 расширенный атрибут a от имени пользователя guest (рис. [-@fig:004		]).

		chattr +a /home/guest/dir1/file1

![установка расширенных атрибутов а](image/04.png){#fig:004 	width=70%}

Потом я открыл другой консоль и там я выполнил команду для установки расширенных атрибутов а  (рис. [-@fig:005		]).

		chattr +a /home/guest/dir1/file1
		
![установка расширенных атрибутов](image/05.png){#fig:005 	width=70%}

Дальше я от пользователя guest проверил правильнсот установления атрибута (рис. [-@fig:006		]).

		lsattr /home/guest/dir1/file1

![проверка](image/06.png){#fig:006 	width=70%}


Затем я выполнил команду чтобы дозапись в файл file1 слова "test" (рис. [-@fig:007		]).

		echo "test" >> /home/guest/dir1/file1

![запись в файл file1](image/07.png){#fig:007 	width=70%}


Потом я проверил что слово правильно записался  (рис. [-@fig:008		]).

		cat /home/guest/dir1/file1

![проверка](image/08.png){#fig:008 	width=70%}


Дальше я попрововал удалить файл file1 либо стереть имеющуюся в нём информацию (рис. [-@fig:009		]).

		echo "abcd" > /home/guest/dir1/file1
		rm file1
		mv file1 file2


![попытки дейтсвий над файлом ](image/09.png){#fig:009 	width=70%}

![попытки дейтсвий над файлом ](image/10.png){#fig:010 	width=70%}

![попытки дейтсвий над файлом ](image/11.png){#fig:011 	width=70%}

 
Дальше я выполнил команду для изменения прав доступа файла file1 (рис. [-@fig:012		]).

		chmod 000 file1

![изменение прав доступа](image/12.png){#fig:012 	width=70%}

Потом я снял расширенный атрибут a с файла file1 от имени суперпользователя  (рис. [-@fig:013		]).

		chattr -a /home/guest/dir1/file1

![снятие расширенного атрибута](image/13.png){#fig:013 	width=70%}

Потом я повторил все шаги но используя атрибут -i  ( от рис. [-@fig:014		]  до рис. [-@fig:021		]  ).

![повторение шагов с меткой -i](image/14.png){#fig:014 	width=70%}

![повторение шагов с меткой -i](image/15.png){#fig:015 	width=70%}

![повторение шагов с меткой -i](image/16.png){#fig:016 	width=70%}

![повторение шагов с меткой -i](image/17.png){#fig:017 	width=70%}

![повторение шагов с меткой -i](image/18.png){#fig:018 	width=70%}

![повторение шагов с меткой -i](image/19.png){#fig:019 	width=70%}

![повторение шагов с меткой -i](image/20.png){#fig:020 	width=70%}

![повторение шагов с меткой -i](image/21.png){#fig:021 	width=70%}





# Выводы

В эту лабораторную работу я смог улучшить мои навыки о работе атрибутов в Linux

# Список литературы{.unnumbered}

::: {#refs}
:::
