---
## Front matter
title: "Отчёта по лабораторной работе №1"
subtitle: "Дисциплина: архитектура компьютера и операционные системы"
author: "Армихос Гонзалез Карла София"

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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.


# Задание

1. Установите виртуальную машину.
2. Установите универсальную утилиту для работы с текстовыми форматами.
3. Узнать информацию о виртуальной машине.

# Теоретическое введение

Операционная система(ОС)—это комплекс взаимосвязанных программ, предназначенных для управления ресурсами компьютера и организации взаимодействия с пользователем. Сегодня наиболее известными операционными системами являются ОС семейства Microsoft Windows и UNIX-подобные системы.

 Дистрибутив GNU Linux — общее определение ОС, использующих ядро Linux и набор библиотек и утилит, выпускаемых в рамках проекта GNU, также графическую оконную подсистему X Window System. Дистрибутив готов для конечной установки на пользовательское оборудование. Кроме ядра и, собственно, операционной системы дистрибутивы обычно содержат широкий набор приложений, таких как редакторы документов и таблиц, мультимедийные проигрыватели, системы для работы с базам и данных ит.д. Существуют дистрибутивы, разрабатываемые как при коммерческой поддержке (Red Hat / Fedora, SLED / OpenSUSE, Ubuntu), так и исключительно усилиями добровольцев (Debian, Slackware, Gentoo, ArchLinux).
 

# Выполнение лабораторной работы

## Выполнение арифметических операций в NASM
Мы открываем нашу виртуальную машину, на которой будем работать (рис 4.1). 
![рис. 4.1 VirtualBox]{#рис.-4.1-virtualbox}

Мы проверяем, что у нас установлен pandoc, в противном случае установите его (рис. 4.2)
![рис. 4.2  Install pandoc] {#рис.-4.2-install-pandoc}

Мы проверяем, что у нас установлен Texlive, в противном случае установите его (рис. 4.3)
![image3]рис. 4.3 Texlive]  {#рис.-4.3-texlive}


# Задание для самостоятельной работы

Выполнив команду  dmesg (рис. 5.1 и 5.2).
![рис. 5.1 dmesg]  {#рис.-5.1-dmesg}

![][image5]**

рис. 5.2 dmesg {#рис.-5.2-dmesg}

Можно использовать поиск с помощью grep для получения информации о версии, процессоре, файлах (рис 5.3, 5.4, 5.5)

![][image6]рис. 5.3  Linux version, CPU0  {#рис.-5.3-linux-version,-cpu0}
![][image7]
рис 5.4 Hypervisor detected, Dev {#рис-5.4-hypervisor-detected,-dev}
![][image8]
рис. 5.5 mount, memory {#рис.-5.5-mount,-memory}


# Выводы

В этой работе вы могли бы узнать немного больше о виртуальной машине, о том, как вы на ней работаете, об основных используемых командах.
Также имеется актуальная информация о его структуре, интерьере.
Кроме того, мы также смогли добавить конвертеры из одного отмеченного формата в другой.


#Контрольные вопросы 

1. **Какую информацию содержит учётная запись пользователя?**
Учётная запись пользователя в Linux содержит:

* UID (User ID) – уникальный идентификатор пользователя. 
* GID (Group ID) – идентификатор группы, к которой принадлежит пользователь. 
* Домашний каталог – личная папка пользователя (обычно /home/username). 
* Интерпретатор команд (Shell) – программа, выполняющая команды (например, /bin/bash). 
* Пароль (захешированный) – хранится в /etc/shadow. 
* Дополнительные группы – группы, к которым пользователь имеет доступ.


2. **Укажите команды терминала и приведите примеры:** 
     
* Получение справки по команде 
  man ls – открывает руководство по команде ls. 
  ls \--help – выводит краткую справку по ls.

* Перемещение по файловой системе

cd /home/user – перейти в /home/user.

cd .. – перейти на уровень выше.

cd \~ – перейти в домашнюю директорию.

cd \- – вернуться в предыдущую директорию.

* Просмотр содержимого каталога

ls – показать файлы в текущем каталоге.

ls \-l – подробный список файлов.

ls \-a – показать скрытые файлы.

ls \-lh – отобразить размер файлов в читаемом формате.

* Определение объёма каталога

du \-sh /home/user – показать размер каталога /home/user.

du \-h \--max-depth=1 – показать размер всех подпапок в текущей директории.

* Создание / удаление каталогов / файлов

mkdir new\_folder – создать каталог new\_folder.

rmdir empty\_folder – удалить пустую папку.

rm file.txt – удалить файл file.txt.

rm \-r folder – удалить папку folder с её содержимым.

touch newfile.txt – создать пустой файл newfile.txt.

* Задание определённых прав на файл / каталог

chmod 755 script.sh – устанавливает права rwxr-xr-x.

chmod \+x script.sh – делает файл исполняемым.

chown user:group file.txt – смена владельца и группы файла.

chown \-R user:group folder/ – смена владельца всех файлов в папке.

* Просмотр истории команд

history – показать историю команд.

history | grep ls – показать все команды, содержащие ls.

\!50 – выполнить команду номер 50 из истории.

\!\! – повторить последнюю команду.

**3\. Что такое файловая система? Приведите примеры с краткой характеристикой.**

Файловая система – это способ организации и хранения данных на диске. Она определяет структуру файлов и папок, а также правила доступа.

* ext4 – стандартная файловая система Linux, поддерживает журналы.  
* NTFS – файловая система Windows, поддерживает права доступа.

**4\. Как посмотреть, какие файловые системы подмонтированы в ОС?**

* mount – показывает все смонтированные файловые системы.  
* df \-T – выводит информацию о файловых системах и их типах.  
* lsblk \-f – показывает файловые системы на подключённых дисках.  
* cat /proc/mounts – выводит список монтированных файловых систем.


**5\. Как удалить зависший процесс?**

* kill PID – завершает процесс с указанным PID.  
* kill \-9 PID – принудительно завершает процесс.  
* pkill process\_name – завершает процесс по имени.  
* htop – интерактивный мониторинг процессов (вы можете убить процесс вручную).  
* ps aux | grep program – найти PID зависшего процесса.  
* killall process\_name – убивает все процессы с указанным именем.


# Список литературы{.unnumbered}

1. [os-intro\_\_02.03.00: Лабораторная работа № 1](https://esystem.rudn.ru/mod/page/view.php?id=1224368#orga7fe648)  
2. [Los 40 comandos de Linux más utilizados en 2025 con ejemplos](https://www.hostinger.com/es/tutoriales/linux-comandos)  
3. [Sistema de archivos: definición y lista de los más importantes \- IONOS](https://www.ionos.com/es-us/digitalguide/servidores/know-how/sistemas-de-archivos/)

