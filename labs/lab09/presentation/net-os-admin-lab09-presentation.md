---
## Front matter
lang: ru-RU
title: Лабораторная работа №9
subtitle: Настройка POP3/IMAP сервера
author:
  - Акунаева Антонина Эрдниевна
institute:
  - Российский университет дружбы народов, Москва, Россия
  
date: 2026-10-31

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

- Приобретение практических навыков по установке и простейшему конфигурированию POP3/IMAP-сервера.  

1. Установите на виртуальной машине server Dovecot и Telnet для дальнейшей проверки корректности работы почтового сервера (см. раздел 9.4.1).  

2. Настройте Dovecot (см. раздел 9.4.2).  

3. Установите на виртуальной машине client программу для чтения почты Evolution и настройте её для манипуляций с почтой вашего пользователя. Проверьте корректность работы почтового сервера как с виртуальной машины server, так и с виртуальной машины client (см. раздел 9.4.3).  

4. Измените скрипт для Vagrant, фиксирующий действия по установке и настройке Postfix и Dovecote во внутреннем окружении виртуальной машины server, создайте скрипт для Vagrant, фиксирующий действия по установке Evolution во внутреннем окружении виртуальной машины client. Соответствующим образом внесите изменения в Vagrantfile (см. раздел 9.4.4).  

# Материалы и методы

- Linux (дистрибутив Rocky 10.2)
- Linux Fedora Workstation (Markdown)
- Oracle VirtualBox 7.2.16
- Vagrant 2.4.9 (Windows amd64)
- Dovecot
- Postfix
- Telnet

# Выполнение лабораторной работы

## Установка dovecot и telnet

![](image/1.PNG){#fig:001 width=70%}

## Конфигурационный файл /etc/dovecot/dovecot.conf

![](image/2.PNG){#fig:002 width=70%}

## Конфигурационный файл /etc/dovecot/conf.d/10-auth.conf

![](image/3.PNG){#fig:003 width=70%}

## Конфигурационный файл /etc/dovecot/conf.d/auth-system.conf.ext

![](image/4.PNG){#fig:004 width=70%}

## Конфигурационный файл /etc/dovecot/conf.d/auth-system.conf.ext

![](image/5.PNG){#fig:005 width=70%}

## Конфигурационный файл /etc/dovecot/conf.d/10-mail.conf

![](image/6.PNG){#fig:006 width=70%}

## Задание каталога доставки почты Postfix

![](image/7.PNG){#fig:007 width=70%}

## Настройка межсетевого экрана

![](image/8.PNG){#fig:008 width=70%}

## Запуск и начало работы с Dovecot

![](image/9.PNG){#fig:009 width=70%}

## Мониторинг работы почтовой службы

![](image/10.PNG){#fig:010 width=70%}

## Установка почтового клиента evolution на client

![](image/11.PNG){#fig:011 width=70%}

## Настройка учётной записи Evolution

![](image/12.PNG){#fig:012 width=70%}

## Настройка учётной записи Evolution

![](image/13.PNG){#fig:013 width=70%}

## Настройка учётной записи Evolution

![](image/14.PNG){#fig:014 width=70%}

## Отправление текстовых писем в Evolution

![](image/15.PNG){#fig:015 width=70%}

## Мониторинг работы почтовой службы

![](image/16.PNG){#fig:016 width=70%}

## Проверка работы почтовой службы через Telnet

![](image/17.PNG){#fig:017 width=70%}

## Изменение внутреннего окружения Vagrant

![](image/18.PNG){#fig:018 width=70%}

## Изменение конфигурационного файла /vagrant/provision/server/mail.sh

![](image/19.PNG){#fig:019 width=70%}

## Изменение конфигурационного файла /vagrant/provision/client/mail.sh

![](image/20.PNG){#fig:020 width=70%}


# Выводы

Я приобрела практическик навыки по установке и простейшему конфигурированию POP3/IMAP-сервера.

