---
## Front matter
title: "Лабораторная работа №6"
subtitle: "Отчёт"
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




# Выполнение лабораторной работы

Проверим,что SELinux работает в режиме enfording и

посмотрим переключатели SELinux для httpd (рис. [-@fig:001]).

![Переключатели SELinux](image/1.png){#fig:001}

Посмотрим на количество типов, пользователей и ролей с помощью команды seinfo (рис. [-@fig:002]).

![seinfo](image/2.png){#fig:002}

Создадим файл /var/www/html/test.html и заполним его одним словом (рис. [-@fig:003]).

![/var/www/html/test.html](image/3.png){#fig:003}

При открытии браузера открывается созданная нами страница (рис. [-@fig:004]).

![Открытие страницы](image/4.png){#fig:004}

Затем посмотрим на метки в директории /var/www/html/ и попробуем сменить метку созданного нами файла и посмотрим логи.

После смены метки доступ к странице был запрещён (рис. [-@fig:005]).

![Доступ запрещён](image/5.png){#fig:005}

Перезагрузим службу. После этого мы не сможем зайти на нашу страницу. Об этом также будут писать логи(рис. [-@fig:006]).

![Смена порта](image/6.png){#fig:006}

Для того, чтобы получилось зайти, досаточно добавить 81 порт в semanage. После Этого вернём всё как было (рис. [-@fig:007]).

![Добавление порта и возврат к первоначальной конфигурации](image/7.png){#fig:007}

При добавленном порте сайт работает, но нам необходимо указать что мы обращаемся именно к этому - 81 порту 

после удаляем порт - что нам не удается и затем удаляем директорию сайта (рис. [-@fig:008]).

![Смена порта обратно](image/8.png){#fig:008}

# Выводы

В результате выполнения лабораторной работы нами было получено понимание работы мандатного разграничения доступа

# Список литературы{.unnumbered}

::: {#refs}
:::
