---
## Front matter
lang: ru-RU
title: презентация лабораторной работы №3
subtitle: Дискреционное разграничение прав в Linux
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



# Порядок выполнения работы

## Создание Пользователей

:::::::::::::: {.columns align=center}
::: {.column}

- Команды
  - useradd guest
  - passwd guest
  - useradd guest2
  - passwd guest2
  - gpasswd -a guest2 guest

:::

::: {.column width="80%"}

![](./image/04.png)

:::
::::::::::::::


## Вход в систему от двух пользователей
:::::::::::::: {.columns align=center}
::: {.column}

![](./image/05.png)

:::

::: {.column}

![](./image/06.png)

:::
::::::::::::::


## определение директорий
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - pwd

![](./image/07.png)

:::

::: {.column}
- команды:
   - pwd
![](./image/08.png)

:::
::::::::::::::


## информация о пользователях
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - groups guest
![](./image/09.png)

:::

::: {.column}

- команды:
   - groups guest2

![](./image/10.png)

:::
::::::::::::::


## информация о пользователе Root
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - id -Gn
   - id -G

:::

::: {.column}


![](./image/13.png)

:::
::::::::::::::


## Сравнение информации пользователей
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - cat /etc/group

:::

::: {.column}


![](./image/14.png)

:::
::::::::::::::

## Регистрация пользователя guest2
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - newgrp guest

:::

::: {.column}


![](./image/16.png)

:::
::::::::::::::


## изменение прав доступа 
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - chmod g+rwx /home/guest

:::

::: {.column}


![](./image/17.png)

:::
::::::::::::::


## Снятие атрибутов
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - chmod 000 home/guest/dir1

:::

::: {.column}


![](./image/18.png)

:::
::::::::::::::

## Проверка атрибутов
:::::::::::::: {.columns align=center}
::: {.column}

- команды:
   - ls -l home/guest

:::

::: {.column}


![](./image/20.png)

:::
::::::::::::::








