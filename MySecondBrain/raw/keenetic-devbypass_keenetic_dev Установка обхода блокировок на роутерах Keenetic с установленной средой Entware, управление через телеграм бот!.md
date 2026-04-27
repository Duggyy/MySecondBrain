---
title: "keenetic-dev/bypass_keenetic_dev: Установка обхода блокировок на роутерах Keenetic с установленной средой Entware, управление через телеграм бот!"
source: "https://github.com/keenetic-dev/bypass_keenetic_dev"
author:
published:
created: 2026-04-27
description: "Установка обхода блокировок на роутерах Keenetic с установленной средой Entware, управление через телеграм бот! - keenetic-dev/bypass_keenetic_dev"
tags:
  - "clippings"
---
## bypass\_keenetic - 💯% free

## Установка обхода блокировок на роутерах Keenetic с установленной средой Entware, управление через телеграм бот. Обхода блокировок много не бывает!

[![](https://github.com/keenetic-dev/bypass_keenetic_dev/raw/main/bypass_keenetic.jpg)](https://github.com/keenetic-dev/bypass_keenetic_dev/blob/main/bypass_keenetic.jpg)

## Что это и зачем

- [Полное описание читайте в вики](https://github.com/znetworkx/bypass_keenetic/wiki)

## Возможности и преимущества

- открытые исходники, полностью **бесплатно**
- управление **через ВАШ телеграм бот** (да, у вас будет свой бот:-)
- поддержка vpn (wireguard, sstp, l2tp, etc)
- поддержка shadowsocks, tor
- **все устройста подключенные к вашему Keenetic смогут открывать сайты из списка** (tv, phone, pc, tablet, etc)!
- можно подключаться к роутеру из вне по vpn и обход будет работать даже если вы не дома
- удобное обновление ключей, мостов и списка адресов
- **безопасная маршрутизация**, трафик vpn идет только к тем сайтам, что указаны в списках, вы спокойно можете использовать госуслуги, интернет-банки (**безопасно!**)
- дальнейшее обновление одним кликом
- поддержка на [форуме](https://forum.keenetic.com/topic/14672-%D0%BE%D0%B1%D1%85%D0%BE%D0%B4%D0%B0-%D0%B1%D0%BB%D0%BE%D0%BA%D0%B8%D1%80%D0%BE%D0%B2%D0%BE%D0%BA-%D0%BC%D0%BD%D0%BE%D0%B3%D0%BE-%D0%BD%D0%B5-%D0%B1%D1%8B%D0%B2%D0%B0%D0%B5%D1%82) и [чате телеграм](https://t.me/bypass_keenetic)

## Установка (~30-60 минут с нуля)

- [Установка Entware](https://github.com/znetworkx/bypass_keenetic/wiki/Install-Entware-and-Preparation)
- [Установка бота и скриптов](https://github.com/znetworkx/bypass_keenetic/wiki/Install-bot-and-scripts)

## Как обновиться:

- [Обновление на новую версию](https://github.com/znetworkx/bypass_keenetic/wiki/Update-bot-and-scripts)

## Если у вас версия 2.0

- `opkg update`
- `mv /opt/etc/bot.py /opt/etc/bot_old.py`
- `curl -o /opt/etc/bot.py https://raw.githubusercontent.com/znetworkx/bypass_keenetic/main/bot.py`
- `bot_pid=$(ps | grep bot.py | awk '{print $1}')`
- `for bot in ${bot_pid}; do kill "${bot}"; done`
- `python3 /opt/etc/bot.py`
- Открыть бота в телеграм -> `/update`
- Наблюдать за процессом обновления. 🔭

> - **Бот перезагрузится сам, нужно просто немного подождать, секунд 30.**
> - **Для корректной работы, возможно потребуется перезагрузить роутер**, в меню бота `Сервис` -> `Перезагрузить роутер`
> - **ВАЖНО: Ключи, мосты, списки сайтов НЕ ПЕРЕЗАПИСЫВАЮТСЯ, в папке `/opt/root/backup-data` будут лежать файлы которые были заменены**

Поддержать проект:

- **znetworkx aka NetworK**
- `4817760309908527` Сбербанк VISA
- **tas-unn aka Masterland**
- `2204120100988217` КАРТА МИР
- `410017539693882` Юмани
- `bc1qesjaxfad8f8azu2cp4gsvt2j9a4yshsc2swey9` Биткоин кошелёк