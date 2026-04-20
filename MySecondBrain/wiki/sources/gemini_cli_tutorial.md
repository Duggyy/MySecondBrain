---
title: "Gemini CLI — полностью бесплатный аналог Claude Code"
type: source
tags: [gemini-cli, free, claude-code-alternative, google, telegram, memory]
lang: ru
created: 2026-04-18
source_file: raw/free_access/Gemini CLI полностью бесплатный аналог Claude Code и Codex  Полная настройка Gemini CLI.md
author: Игорь Зуевич
published: 2026-04-18
source_url: "https://www.youtube.com/watch?v=RzSbZr2orEQ"
---

## Описание

Gemini CLI — бесплатный AI-ассистент от Google, полный аналог Claude Code и Codex. Работает на сервере, управляется через терминал или Telegram-бот.

## Ключевые преимущества

| Параметр | Gemini CLI | Claude Code |
|----------|------------|-------------|
| Цена | Бесплатно | $20+/месяц |
| Context window | 2,000,000 tokens | 200,000 tokens |
| Google Workspace | По умолчанию | Требует настройки |
| Голосовые | Встроены | Требуют Groq API |

## Лимиты

- **Бесплатный тариф**: 1,000 запросов/день
- **С API ключом**: 250 запросов/день
- **Установка через npm**: `npx gemini-cli`

## Архитектура настройки (12 файлов)

1. Установка Node.js 22
2. Авторизация через Google
3. Создание структуры папок проекта
4. Telegram Bridge (мост с Telegram)
5. Мультимодальность (фото, голос, документы)
6. Трёхслойная память (SQLite + Agent + Obsidian)
7. Продвинутая архитектура и сжатие контекста
8. Подключение внешних инструментов (Firecrawl, n8n)
9. Планировщик задач
10. Система команд для Telegram
11. Продакшн-чеклист
12. Автозапуск

## Память: три слоя

- **SQLite memory** — быстрое хранение
- **Agent memory** — интеллектуальная обработка
- **Obsidian memory** — wiki для долгосрочного хранения

## Telegram-мост

Позволяет управлять Gemini CLI через Telegram:
- Голосовые сообщения
- Отправка документов
- Команды через меню
- Автоматические задачи по расписанию

## Статус

**Active** — Gemini CLI развивается, добавляются новые функции бесплатно.

## Связанные концепты

- [[cliclaw_tutorial|CliClaw]] — альтернативный Telegram-агент
- [[memory_system_taxonomy|Memory System Taxonomy]] — трёхслойная память

[[index|← Назад к индексу]]