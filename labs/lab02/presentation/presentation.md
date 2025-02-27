---
## Front matter
lang: ru-RU
title: лабораторной работы №2
subtitle: Установка и конфигурация операционной системы на виртуальную машину
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

# Создание нового пользователя

## новый пользователь

:::::::::::::: {.columns align=center}
::: {.column}
- useradd guest

:::

::: {.column width="80%"}

![](./image/01.png)

:::
::::::::::::::

## создание пароля

:::::::::::::: {.columns align=center}
::: {.column}
- passwd guest

:::

::: {.column width="80%"}

![](./image/02.png)

:::
::::::::::::::

# вход в систему с новым пользователем

## новый пользователь

:::::::::::::: {.columns align=center}

::: {.column width="80%"}

![](./image/101.jpg)

:::
::::::::::::::


## проверка директории

:::::::::::::: {.columns align=center}
::: {.column}

- pwd

:::

::: {.column width="80%"}

![](./image/04.png)

:::
::::::::::::::

## проверка пользователя

:::::::::::::: {.columns align=center}
::: {.column}

- whoami

:::

::: {.column width="80%"}

![](./image/05.png)

:::
::::::::::::::

## информация пользователя

:::::::::::::: {.columns align=center}
::: {.column}

- id

:::

::: {.column width="80%"}

![](./image/06.png)

:::
::::::::::::::

## проверка группы пользователя

:::::::::::::: {.columns align=center}
::: {.column}

- groups

:::

::: {.column width="80%"}

![](./image/07.png)

:::
::::::::::::::

## файл /etc/paswd

:::::::::::::: {.columns align=center}
::: {.column}

- cat /etc/passwd

:::

::: {.column width="80%"}

![](./image/08.png)

:::
::::::::::::::

## мой пользователь guest

:::::::::::::: {.columns align=center}
::: {.column}

- cat /etc/passwd | grep guest

:::

::: {.column width="80%"}

![](./image/09.png)

:::
::::::::::::::

## cуществующие в системе директории

:::::::::::::: {.columns align=center}
::: {.column}

- ls -l /home/

:::

::: {.column width="80%"}

![](./image/10.png)

:::
::::::::::::::


## расширенные атрибуты установлены

:::::::::::::: {.columns align=center}
::: {.column}

- lsattr /home

:::

::: {.column width="80%"}

![](./image/11.png)

:::
::::::::::::::

## новый каталог

:::::::::::::: {.columns align=center}
::: {.column}

- mkdir dir1

:::

::: {.column width="80%"}

![](./image/12.png)

:::
::::::::::::::

## определение прав доступа и расширенные атрибуты

:::::::::::::: {.columns align=center}
::: {.column}

- ls -l
- lsattr

:::

::: {.column width="80%"}

![](./image/13.png)

:::
::::::::::::::


## изменение атрибутов

:::::::::::::: {.columns align=center}
::: {.column}

- chmod 000 dir1

:::

::: {.column width="80%"}

![](./image/14.png)

:::
::::::::::::::


## попытка создания нового файла

:::::::::::::: {.columns align=center}
::: {.column}

- echo "test" > /home/guest/dir1/file1

:::

::: {.column width="80%"}

![](./image/15.png)

:::
::::::::::::::

## проверка создания

:::::::::::::: {.columns align=center}
::: {.column}

- ls -l /home/guest/dir1

:::

::: {.column width="80%"}

![](./image/16.png)

:::
::::::::::::::




# таблица прав доступа

## таблица прав доступа
:::::::::::::: {.columns align=center}
::: {.column}

- example

:::

::: {.column width="80%"}

![](./image/16.png)

:::
::::::::::::::




