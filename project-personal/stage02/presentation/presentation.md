---
## Front matter
lang: ru-RU
title: Индивидуальный проект этап 2
subtitle: Презентация
author:
  - Коровкин Н.М
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 10 марта 2026


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
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
 
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Коровкин Никита Михайлович
  * Студент
  * Российский университет дружбы народов
  * [1132246835@pfur.ru](mailto:1132246835@pfur.ru)

:::
::: {.column width="30%"}

:::
::::::::::::::

## Цель работы

Установить DVWA

## Выполнение лабораторной работы

Вводим предложенную на странице гитхаба команду для автоматической установки. Начнётся установка, и сначала установится php-gd (рис. [-@fig:001]).

![Ввод команды](image/1.png){#fig:001}

## Выполнение лабораторной работы


После этого переходим на предложенный адрес localhost/dvwa и нажимаем на reset database (рис. [-@fig:002]).

![Переход на сайт](image/2.png){#fig:002}

## Выполнение лабораторной работы

После этого авторизируемся по тем данным, что были выведены на скриншоте 2 (рис. [-@fig:003]).

![Авторизация](image/3.png){#fig:003}

## Выполнение лабораторной работы


И мы заходим на настроенный сайт 

## Выводы

Был настроен dvwa

## Список литературы{.unnumbered}

::: {#refs}
:::

