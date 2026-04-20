---
title: "Создай AI-агента за 10 минут | CliClaw"
type: source
tags: [ai-agent, cliclaw, telegram, openrouter, gemini, claude-code, free]
lang: ru
created: 2026-04-20
source_file: raw/ai_agents/Создай AI-агента за 10 минут бесплатно  CliClaw гайд 2026.md
author: Вайбкодим бабки | Андрей Присекин
published: 2026-04-19
source_url: "https://www.youtube.com/watch?v=7_x-QmoDwrI"
---

## Описание

Бесплатный AI-агент CliClaw — замена QwenClaw (который закрыл бесплатный доступ). Устанавливается на VPS, работает через Telegram.

## Ключевые возможности

- **Мультимодельность**: Claude Code, Codex, Gemini, OpenRouter (любая бесплатная модель)
- **Персистентная память**: факты сохраняются между сессиями и не зависят от модели
- **Переключение на лету**: можно менять модель без потери памяти
- **Voice input**: распознавание голосовых через Groq API
- **Планировщик**: напоминания и scheduled tasks

## Архитектура

- VPS (Ubuntu 24.04, ~$1-5/месяц)
- Telegram bot как интерфейс
- OpenRouter / Claude Code / Gemini как бэкенд
- Память хранится на сервере в файлах

## Поддерживаемые модели

| Модель | Тип | Лимиты |
|--------|-----|--------|
| Claude Code | Клиент | Требуется подписка ($25) |
| Codex | Клиент | Требуется подписка ($25) |
| Gemini | API | 60 req/min (light), 10 req/min (heavy) |
| OpenRouter | API | Меняется, проверять бесплатные модели |

## Ограничения

- Через API (OpenRouter, Gemini): базовые функции работают (память, напоминания)
- File editing / code writing на сервере: только через клиент (Claude Code/Codex)
- Бесплатные модели OpenRouter меняются со временем

## Установка

1. Арендовать VPS (не в РФ)
2. Создать Telegram бота через BotFather
3. Получить API ключи: Groq (для голоса), OpenRouter
4. Склонить репозиторий и запустить install скрипт
5. Авторизоваться через браузер

## Связанные инструменты

- [[qwenclaw|QwenClaw]] — предшественник (бесплатный доступ закрыт)
- [[gemini_cli|Gemini CLI]] — альтернативный бесплатный CLI-агент

[[index|← Назад к индексу]]