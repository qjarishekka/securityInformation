---
## Front matter
lang: ru-RU
title: презентация лабораторной работы №4
subtitle: Дискреционное разграничение прав в Linux. Расширенные атрибуты
author:
  - Кхари Жекка Кализая Арсе

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# выполнение лабораторной работы

## определение расширенных атрибутов

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:
	- lsattr /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/02.png)

:::
::::::::::::::

## установка расширенных атрибутов

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:
	- chmod 600 file1
	- chattr +a /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/04.png)

:::
::::::::::::::

## установка расширенных атрибутов от суперпользователя

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chattr +a /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/05.png)

:::
::::::::::::::


## проверка правильности установления атрибута

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- lsattr /home/dir1/file1

:::
::: {.column width="30%"}

![](./image/06.png)

:::
::::::::::::::

## действия над файлом file1

## дозапись 

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- echo "test" >> /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/08.png)

:::
::::::::::::::


## удаление 

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- rm file1

:::
::: {.column width="30%"}

![](./image/09.png)

:::
::::::::::::::



## стереть имеющуюся в нём информацию 

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- echo "abcd" > /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/10.png)

:::
::::::::::::::

## переименование

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- mv file1 file2

:::
::: {.column width="30%"}

![](./image/11.png)

:::
::::::::::::::




## Снятие прав доступа

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chmod 000 file1

:::
::: {.column width="30%"}

![](./image/12.png)

:::
::::::::::::::


## снятие раширенных атрибутов с файла file1

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chattr -a /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/13.png)

:::
::::::::::::::

## вторая попытка снятия прав доступа

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chmod 000 file1

:::
::: {.column width="30%"}

![](./image/13.png)

:::
::::::::::::::

# повторение шагов используя расширенный атрибут i

## изменение прав доступа

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chmod 000 file1

:::
::: {.column width="30%"}

![](./image/14.png)

:::
::::::::::::::

## установка расширенных атрибутов от суперпользователя

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chattr +a /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/15.png)

:::
::::::::::::::


## проверка правильности установления атрибута

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- lsattr /home/dir1/file1

:::
::: {.column width="30%"}

![](./image/16.png)

:::
::::::::::::::

## действия над файлом file1

## дозапись 

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- echo "test" >> /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/17.png)

:::
::::::::::::::






## стереть имеющуюся в нём информацию 

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- echo "abcd" > /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/17.png)

:::
::::::::::::::

## переименование

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- mv file1 file2

:::
::: {.column width="30%"}

![](./image/18.png)

:::
::::::::::::::




## Снятие прав доступа

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chmod 000 file1

:::
::: {.column width="30%"}

![](./image/19.png)

:::
::::::::::::::


## снятие раширенных атрибутов с файла file1

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chattr -a /home/guest/dir1/file1

:::
::: {.column width="30%"}

![](./image/20.png)

:::
::::::::::::::

## вторая попытка снятия прав доступа

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

- команды:

	- chmod 000 file1

:::
::: {.column width="30%"}

![](./image/21.png)

:::
::::::::::::::



# Спасибо за внимание


