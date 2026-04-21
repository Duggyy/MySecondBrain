---
title: Claude Routines
type: source
tags: [claude, automation, routines, cron, github]
lang: ru
created: 2026-04-21
sources: [Claude Routines.md]
---

# Claude Routines — автоматизации 24/7

## Ситуация
Рутинные задачи (дайджесты, мониторинг) требуют ручного запуска каждый день

## Решение
Claude Routines — автоматизации на серверах Anthropic. Компьютер выключен — задачи выполняются.

## Триггеры
- По расписанию (cron)
- По API запросу
- По событиям GitHub

## Лимиты
| Тариф | Запусков/сут |
|-------|-------------|
| Pro | 5 |
| Max | 15 |
| Team | 25 |

## Настройка
1. GitHub коннектор (Settings → Connectors)
2. Приватный репозиторий
3. New Routine → Remote
4. Environment для API ключей (TG bot, etc.)
5. White List домены (custom)
6. Permissions — НЕ давать запись в main branch!

## Пример: Gmail → Telegram
1. Gmail коннектор
2. Claude анализирует письма
3. Telegram бот отправляет отчет

## Пример: AI Digest
YouTube + GitHub + Telegram → единый дайджест в Telegram

## Безопасность
API ключи — ТОЛЬКО в Environment, не в промт!

## Источник
Матвей Шульга, 2026-04-20
