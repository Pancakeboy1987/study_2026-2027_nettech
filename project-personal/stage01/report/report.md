---
## Front matter
title: "Отчёт по индивидуальному проекту"
subtitle: "Часть 1"
author: "Коровкин Никита Михайлович"

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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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

Установить Kali Linux

# Выполнение лабораторной работы

Выделим память и процессоры 

Выделим диск

Выберим загрузочный образ и имя VM (рис. [-@fig:001]).

![Выделение памяти и процессоров, название](image/1.png){#fig:001}

После запуска выберем английский язык (рис. [-@fig:002]).

![Настройка языка](image/2.png){#fig:002}

Настроим клавишу для переключения языка (рис. [-@fig:003]).

![Клавиша переключения языка](image/3.png){#fig:003}

Выберем имя для компьютера (рис. [-@fig:004]).

![Имя компьютера](image/4.png){#fig:004}

Выберем имя домена (рис. [-@fig:005]).

![Имя домена](image/4.png){#fig:005}

Выберем имя пользователя и настроим пароль.

Сделаем авто разметку дисков

Выберем диск для установки и настроим дополнительные параметры установки 

Завершение установки (рис. [-@fig:006]).

![Завершение установки](image/5.png){#fig:006}

# Выводы

В результате выполнения лабораторной работы был установлен kali linux

# Список литературы{.unnumbered}

::: {#refs}
:::
