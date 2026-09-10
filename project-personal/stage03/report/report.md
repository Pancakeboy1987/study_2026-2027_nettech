---
## Front matter
title: "Отчёт по индивидуальному проекту"
subtitle: "Часть 3"
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

Разобраться в работе Hydra

# Выполнение лабораторной работы

Для начала мы распакуем архив с базой данных паролей (рис. [-@fig:001]).

![Разархивация паролей](image/1.png){#fig:001}

Далее сломаем одно из окон авторизации DVWA. Запомним фразу, которая высвечивается при неправильном пароле, а также данные куки снизу (рис. [-@fig:002]).

![Данные с сайта DVWA](image/2.png){#fig:002}

После этого воспользуемся гидрой. Укажем ей файл с паролями и адрес ломаемого сайта. Укажем также данные куки и фразу, выводящуюся при неверной авторизации, что будет подсказкой для гидры, что пароль неверный. В результате, получаем пароль (рис. [-@fig:003]).

![Использование Hydra](image/3.png){#fig:003}

Вводим пароль на сайт (рис. [-@fig:004]).

![Успешная авторизация](image/4.png){#fig:004}

# Выводы

В результате выполнения лабораторной работы были получены навыки работы с hydra

# Список литературы{.unnumbered}

::: {#refs}
:::
