---
## Front matter
lang: ru-RU
title: Лабораторная работа №11
subtitle: Настройка безопасного удалённого доступа по протоколу SSH
author:
  - Акунаева Антонина Эрдниевна
institute:
  - Российский университет дружбы народов, Москва, Россия
  
date: 2026-11-14

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

- Приобретение практических навыков по настройке удалённого доступа к серверу с помощью SSH.  

1. Настройте запрет удалённого доступа на сервер по SSH для пользователя root (см. раздел 11.4.1).  

2. Настройте разрешение удалённого доступа к серверу по SSH только для пользователей группы vagrant и вашего пользователя (см. раздел 11.4.2).  

3. Настройте удалённый доступ к серверу по SSH через порт 2022 (см. раздел 11.4.3).  

4. Настройте удалённый доступ к серверу по SSH по ключу (см. раздел 11.4.4).  

5. Организуйте SSH-туннель с клиента на сервер, перенаправив локальное соединение с TCP-порта 80 на порт 8080 (см. раздел 11.4.5).  

6. Используя удалённое SSH-соединение, выполните с клиента несколько команд на сервере (см. раздел 11.4.6).  

7. Используя удалённое SSH-соединение, запустите с клиента графическое приложение на сервере (см. раздел 11.4.7).  

8. Напишите скрипт для Vagrant, фиксирующий действия по настройке SSH-сервера во внутреннем окружении виртуальной машины server. Соответствующим образом внесите изменения в Vagrantfile (см. раздел 11.4.8).  

# Материалы и методы

- Linux (дистрибутив Rocky 10.2)
- Linux Fedora Workstation (Markdown)
- Oracle VirtualBox 7.2.16
- Vagrant 2.4.9 (Windows amd64)
- SSH

# Выполнение лабораторной работы

## Подготовка к работе с sshd

![](image/1.PNG){#fig:001 width=70%}

## Мониторинг системных событий

![](image/2.PNG){#fig:002 width=70%}

## Неудачное отключение к root@server.aeakunaeva.net

![](image/3.PNG){#fig:003 width=70%}

## Редактирование /etc/ssh/sshd_config

![](image/4.PNG){#fig:004 width=70%}

## Повторное неудачное подключение к root@server

![](image/5.PNG){#fig:005 width=70%}

## Успешное подключение к aeakunaeva@server.aeakunaeva.net

![](image/6.PNG){#fig:006 width=70%}

## Редактирование /etc/ssh/sshd_config

![](image/7.PNG){#fig:007 width=70%}

## Перезапуск службы sshd

![](image/8.PNG){#fig:008 width=70%}

## Повторное подключение к aeakunaeva@server.aeakunaeva.net

![](image/9.PNG){#fig:009 width=70%}

## Редактирование /etc/ssh/sshd_config

![](image/10.PNG){#fig:010 width=70%}

## Повторное подключение к aeakunaeva@server.aeakunaeva.net

![](image/11.PNG){#fig:011 width=70%}

## Редактирование /etc/ssh/sshd_config

![](image/12.PNG){#fig:012 width=70%}

## Расширенный статус работы sshd

![](image/13.PNG){#fig:013 width=70%}

## Исправление меток SELinux и настройки межсетевого экрана для порта 2022

![](image/14.PNG){#fig:014 width=70%}

## Успешное подключение к aeakunaeva@server.aeakunaeva.net и получение доступа root

![](image/15.PNG){#fig:015 width=70%}

## Успешное подключение к aeakunaeva@server.aeakunaeva.net через порт 2022

![](image/16.PNG){#fig:016 width=70%}

## Редактирование /etc/ssh/sshd_config

![](image/17.PNG){#fig:017 width=70%}

## Генерация ключей SSH

![](image/18.PNG){#fig:018 width=50%}

## Просмотр прослушиваемых служб с протоколом TCP

![](image/19.PNG){#fig:019 width=70%}

## Страница Firefox по порту 8080

![](image/20.PNG){#fig:020 width=70%}

## Просмотр данных сервера с клиента

![](image/21.PNG){#fig:021 width=70%}

## Просмотр данных сервера с клиента

![](image/22.PNG){#fig:022 width=70%}

## Редактирование /etc/ssh/sshd_config

![](image/23.PNG){#fig:023 width=70%}

## Запуск графического приложения сервера с клиента

![](image/24.PNG){#fig:024 width=70%}

## Внесение изменений в настройки внутреннего окружения ВМ

![](image/25.PNG){#fig:025 width=70%}

## Редактирование /vagrant/provision/server/ssh.sh

![](image/26.PNG){#fig:026 width=70%}

## Редактирование Vagrantfile

![](image/27.PNG){#fig:027 width=70%}


# Выводы

Я приобрела практические навыки по настройке удалённого доступа к серверу с помощью SSH.

