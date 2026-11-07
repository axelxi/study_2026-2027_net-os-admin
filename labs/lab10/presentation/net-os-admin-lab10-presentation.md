---
## Front matter
lang: ru-RU
title: Лабораторная работа №10
subtitle: Расширенные настройки SMTP-сервера
author:
  - Акунаева Антонина Эрдниевна
institute:
  - Российский университет дружбы народов, Москва, Россия
  
date: 2026-11-07

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

- Приобретение практических навыков по конфигурированию SMTP-сервера в части настройки аутентификации.  

1. Настройте Dovecot для работы с LMTP (см. раздел 10.4.1).  

2. Настройте аутентификацию посредством SASL на SMTP-сервере (см. раздел 10.4.2).  

3. Настройте работу SMTP-сервера поверх TLS (см. раздел 10.4.3).  

4. Скорректируйте скрипт для Vagrant, фиксирующий действия расширенной настройки SMTP-сервера во внутреннем окружении виртуальной машины server (см. раздел 10.4.4).  

# Материалы и методы

- Linux (дистрибутив Rocky 10.2)
- Linux Fedora Workstation (Markdown)
- Oracle VirtualBox 7.2.16
- Vagrant 2.4.9 (Windows amd64)
- FAR Manager 3.0 build 6699 x64
- Packer 1.16.0 (Windows amd64)
- Postfix
- Dovecot
- Telnet

# Выполнение лабораторной работы

## Настройка LMTP и Dovecot

![](image/1.PNG){#fig:001 width=70%}

## Журнал мониторинга работы почтовой службы

![](image/2.PNG){#fig:002 width=70%}

## Редактирование /etc/dovecot/dovecot.conf

![](image/3.PNG){#fig:003 width=70%}

## Редактирование /etc/dovecot/conf.d/10-master.conf

![](image/4.PNG){#fig:004 width=70%}

## Редактирование etc/dovecot/conf.d/10-auth.conf

![](image/5.PNG){#fig:005 width=70%}

## Отправление письма с client через LMTP

![](image/6.PNG){#fig:006 width=70%}

## Проверка почтового ящика на server

![](image/7.PNG){#fig:007 width=70%}

## Редактирование /etc/dovecot/conf.d/10-master.conf

![](image/8.PNG){#fig:008 width=70%}

## Редактирование /etc/postfix/master.cf

![](image/9.PNG){#fig:009 width=70%}

## Настройка Postfix

![](image/10.PNG){#fig:010 width=70%}

## Установка telnet на client

![](image/11.PNG){#fig:011 width=70%}

## Проверка работы telnet на client

![](image/12.PNG){#fig:012 width=70%}

## Конфигурация Postfix

![](image/13.PNG){#fig:013 width=70%}

## Редактирование /etc/postfix/master.cf

![](image/14.PNG){#fig:014 width=70%}

## Настройка межсетевого экрана

![](image/15.PNG){#fig:015 width=70%}

## Подключение к SMTP-серверу на client

![](image/16.PNG){#fig:016 width=70%}

## Подключение к SMTP-серверу на client

![](image/17.PNG){#fig:017 width=70%}

## Настройка учётной записи Evolution

![](image/18.PNG){#fig:018 width=70%}

## Проверка корректности отправки почтовых сообщений

![](image/19.PNG){#fig:019 width=70%}

## Внесение изменений в настройки внутреннего окружения server

![](image/20.PNG){#fig:020 width=70%}

## Редактирование /vagrant/provision/server/mail.sh

![](image/21.PNG){#fig:021 width=70%}

## Редактирование /vagrant/provision/client/mail.sh

![](image/22.PNG){#fig:022 width=70%}


# Выводы

Я приобрела практические навыки по конфигурированию SMTP-сервера в части настройки аутентификации.

