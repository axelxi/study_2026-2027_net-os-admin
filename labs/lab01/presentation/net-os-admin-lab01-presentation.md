---
## Front matter
lang: ru-RU
title: Лабораторная работа №1
subtitle: Подготовка лабораторного стенда
author:
  - Акунаева Антонина Эрдниевна
institute:
  - Российский университет дружбы народов, Москва, Россия
  
date: 2026-09-12

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

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Акунаева Антонина Эрдниевна
  * студент ФФМиЕН, НПИбд-02-24
  * Российский университет дружбы народов
  * [1032240492@rudn.ru](mailto:1032240492@rudn.ru)
  * <https://github.com/Akuxee>

:::
::: {.column width="30%"}

![](./image/aeakunaeva.PNG)

:::
::::::::::::::

# Цели и задачи

- Целью данной работы является приобретение практических навыков установки Rocky Linux на виртуальную машину с помощью инструмента Vagrant.

1. Сформируйте box-файл с дистрибутивом Rocky Linux для VirtualBox (см. раздел 1.5.2 или 1.5.3).
2. Запустите виртуальные машины сервера и клиента и убедитесь в их работоспособности.
3. Внесите изменения в настройки загрузки образов виртуальных машин server и client, добавив пользователя с правами администратора и изменив названия хостов (см. раздел 1.5.4).
4. Скопируйте необходимые для работы с Vagrant файлы и box-файлы виртуальных машин на внешний носитель. Используя эти файлы, вы можете попробовать развернуть виртуальные машины на другом компьютере.

# Материалы и методы

- Linux (дистрибутив Rocky 10.2)
- Linux Fedora Workstation (Markdown)
- Oracle VirtualBox 7.2.16
- Vagrant 2.4.9 (Windows amd64)
- FAR Manager 3.0 build 6699 x64
- Packer 1.16.0 (Windows amd64)

# Выполнение лабораторной работы

## Создание каталога для проекта

![](image/1.PNG){#fig:001 width=70%}

## Добавление файла vagrant-rocky.pkr.hcl

![](image/2.PNG){#fig:002 width=70%}

## Файл packer/http/rocky10-ks.cfg

![](image/3.PNG){#fig:003 width=70%}

## Файл vagrant/Vagrantfile

![](image/4.PNG){#fig:004 width=70%}

## Подкаталоги vagrant/provision/client default server

![](image/5.PNG){#fig:005 width=70%}

## Файлы подкаталога vagrant/provision/default

![](image/7.PNG){#fig:006 width=70%}

## Файлы подкаталога vagrant/provision/server

![](image/8.PNG){#fig:007 width=70%}

## Файлы подкаталога vagrant/provision/client

![](image/6.PNG){#fig:008 width=70%}

## Установка Rocky Linux при помощи FAR: init

```
packer.exe init vagrant-rocky.pkr.hcl
```

![](image/9.PNG){#fig:009 width=70%}

## Установка Rocky Linux при помощи FAR: build

```
packer.exe build vagrant-rocky.pkr.hcl
```

![](image/10.PNG){#fig:010 width=70%}

## Регистрация образа виртуальной машины

```
vagrant box add rockylinux10 vagrant-virtualbox-rockylinux10-x86_64.box
```

![](image/11.PNG){#fig:011 width=70%}

## Запуск виртуальной машины Server

```
 vagrant up server
```

![](image/12.PNG){#fig:012 width=70%}

## Запуск виртуальной машины Client

```
 vagrant up client
```

![](image/13.PNG){#fig:013 width=70%}

## Подключение к серверу и клиенту из консоли и выход

```
vagrant ssh server/client
su - aeakunaeva
exit
```

![](image/14.PNG){#fig:014 width=70%}

## Проверка файла Vagrantfile

![](image/15.PNG){#fig:015 width=70%}

## Сохранение изменений внутренних настроек ВМ для Server

```
vagrant up server --provision
```

![](image/16.PNG){#fig:016 width=70%}

## Проверка приглашения для Server

![](image/17.PNG){#fig:017 width=70%}

## Сохранение изменений внутренних настроек ВМ для Client

```
vagrant up client --provision
```

![](image/18.PNG){#fig:018 width=70%}


# Выводы

Я приобрела практические навыки установки Rocky Linux на виртуальную машину с помощью инструмента Vagrant.

