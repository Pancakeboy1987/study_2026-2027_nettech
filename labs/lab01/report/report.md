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

Получить практические навыки создания и управления виртуальными машинами с использованием gns3

# Задание

Установка и настройка GNS3 и сопутствующего программного обеспечения.


# Выполнение лабораторной работы

В методических материалах выполнение лабораторной работы рассматривается на Windows. В моём случае работа выполнялась на Linux, так как основной компьютер - MacBook Air с процессором Apple M2. Поэтому вместо установки GNS3 непосредственно на Windows была использована ранее созданная виртуальная машина с Fedora Linux.

Все дальнейшие действия выполнялись внутри Fedora VM: запуск GNS3, установка необходимых пакетов, добавление образов маршрутизаторов и проверка их работы. Такой вариант позволяет выполнить те же этапы лабораторной работы в Linux-среде(рис. [-@fig:001]).

![Работа в Fedora Linux](image/1.png){#fig:01 width=70%}

После проверки системы были установлены GNS3 GUI, GNS3 Server и необходимые дополнительные компоненты. Также были установлены QEMU, libvirt, Telnet и другие инструменты, необходимые для дальнейшей работы.(рис. [-@fig:002]).


![Установка GNS3 и зависимостей](image/2.png){#fig:02 width=70%}

После установки GNS3 был запущен из терминала командой:

gns3
При первом запуске был пройден Setup Wizard. В качестве способа запуска устройств был выбран локальный сервер, поскольку GNS3 Server уже работает непосредственно внутри Fedora.

Порт локального сервера 3080 был оставлен без изменений. После завершения настройки открылось основное окно GNS3. [-@fig:03]

![Первый запуск GNS3](image/3.png){#fig:03 width=70%}

Следующим этапом было добавление маршрутизатора FRR (FRRouting).

В GNS3 был открыт раздел добавления маршрутизаторов, после чего через мастер установки был выбран FRR. Образ был установлен на локальный компьютер и настроен для работы через эмулятор QEMU.

После загрузки и импорта образа был создан шаблон FRR. В настройках шаблона была включена автоматическая генерация диска конфигурации.[-@fig:04]

![Добавление шаблона FRR](image/4.png){#fig:04 width=70%}

Для проверки работоспособности установленного образа был создан новый пустой проект GNS3 с названием PR-01.

В рабочую область был добавлен маршрутизатор FRR. После запуска устройства была открыта консоль, в которой появилось приглашение:

frr#
После этого была выполнена команда:

show version
Она позволила проверить версию установленного FRRouting.[-@fig:05]

![Запуск FRR и команда show version](image/5.png){#fig:05 width=70%}

После проверки FRR аналогичная проверка была выполнена для VyOS.

В проект был добавлен маршрутизатор VyOS, после чего устройство было запущено и открыта его консоль.


show version
В результате была подтверждена версия VyOS 1.3.3.

![Запуск VyOS и команда show version](image/7.png){#fig:06 width=70%}

На рисунке [-@fig:06] показан запущенный маршрутизатор VyOS и результат проверки его версии.



---

# Выводы

Были установлены GNS3 и необходимые зависимости, добавлены и настроены шаблоны FRR и VyOS, отключён KVM для корректной работы в среде Apple Silicon, а также проверена работоспособность обоих маршрутизаторов.


# Список литературы{.unnumbered}

::: {#refs}
:::
