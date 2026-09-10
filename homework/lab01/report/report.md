---
## Front matter
title: "Лабораторная работа №1"
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

Изучить методы кодирования и модуляции сигналов с помощью высокоуровневого языка программирования Octave, определить спектр и параметры сигналов, продемонстрировать принцип аналоговой амплитудной модуляции и исследовать свойство самосинхронизации различных способов кодирования.

# Задание

В ходе выполнения лабораторной работы необходимо:

построить график функции y = sin(x) + 1/3 sin(3x) + 1/5 sin(5x) на интервале [-10; 10];

добавить на один график функцию y = cos(x) + 1/3 cos(3x) + 1/5 cos(5x);

получить графики меандра при различном количестве гармоник и повторить построение через синусы;

определить спектры двух синусоидальных сигналов с частотами 10 и 40 Гц;

скорректировать спектры с учётом отрицательных частот и нормировки;

определить спектр суммы двух сигналов;

выполнить моделирование аналоговой амплитудной модуляции;

реализовать униполярное, AMI, NRZ, RZ, манчестерское и дифференциальное манчестерское кодирование;

исследовать свойство самосинхронизации кодов;

построить спектры полученных кодированных сигналов.





# Выполнение лабораторной работы

Построение графика синусоидальной функции
В первом задании был создан сценарий plot_sin.m. В нём сформирован массив значений x от -10 до 10 с шагом 0.1, после чего вычислена функция:

y = sin(x) + 1/3 sin(3x) + 1/5 sin(5x)(рис. [-@fig:001]).

![График 1](image/1.png){#fig:01 width=70%}

Построение синусоидальной и косинусоидальной функций
Следующим этапом к исходному графику была добавлена функция:

y2 = cos(x) + 1/3 cos(3x) + 1/5 cos(5x)
Обе функции были построены в одной системе координат с использованием hold on.(рис. [-@fig:002]).

![График 2](image/2.png){#fig:02 width=70%}

Разложение меандра в частичный ряд Фурье
Для исследования разложения импульсного сигнала был создан файл meandr.m. В качестве количества гармоник было выбрано N = 8, амплитуда A = 1, период T = 1.(рис. [-@fig:003]).

![График 3](image/3.png){#fig:03 width=70%}

Определение спектров двух синусоидальных сигналов
Для исследования спектра были созданы два сигнала:

частота первого сигнала f1 = 10 Гц, амплитуда a1 = 1;

частота второго сигнала f2 = 40 Гц, амплитуда a2 = 0.7;

частота дискретизации fd = 512 Гц;

длительность сигнала tmax = 0.5 с.

Сигналы задавались выражениями:

signal1 = a1*sin(2*pi*t*f1);
signal2 = a2*sin(2*pi*t*f2);
Сначала были построены временные графики двух сигналов.(рис. [-@fig:004]).

![График 4](image/4.png){#fig:04 width=70%}

По заданным битовым последовательностям я получил кодированные сигналы для нескольких кодов(рис. [-@fig:005]).

![График 5](image/5.png){#fig:05 width=70%}

Следующие графики(рис. [-@fig:006]).

![График 6](image/6.png){#fig:06 width=70%}




---

# Выводы

В ходе лабораторной работы были изучены основные методы представления, кодирования и модуляции сигналов в GNU Octave.

# Список литературы{.unnumbered}

::: {#refs}
:::
