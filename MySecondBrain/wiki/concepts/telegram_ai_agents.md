---
title: "AI-агенты на базе Telegram"
type: concept
tags: [ai-agent, telegram, vps, automation]
lang: ru
created: 2026-04-20
---

## Концепция

AI-агенты на базе Telegram — это автономные ассистенты, работающие через Telegram-бот как интерфейс. Устанавливаются на VPS, поддерживают различные LLM-движки.

## Архитектура

```
Пользователь ←→ Telegram Bot ←→ AI Agent (VPS) ←→ LLM Provider
```

## Популярные реализации

| Агент | Модель | Статус | Особенности |
|-------|--------|--------|-------------|
| [[qwenclaw|QwenClaw]] | Qwen | Deprecated | Бесплатный, лимиты срезаны |
| [[cliclaw_tutorial|CliClaw]] | Claude/Codex/Gemini/OpenRouter | Active | Мультимодельность, память |
| Gemini CLI | Gemini | Active | Бесплатный (60 req/min) |

## Ключевые компоненты

- **VPS**: Ubuntu 24.04, ~$1-5/месяц
- **Telegram Bot**: интерфейс (BotFather)
- **API Keys**: Groq (voice), OpenRouter/Gemini/Claude
- **Память**: персистентная на сервере

## Преимущества

- Работает 24/7
- Персистентная память между сессиями
- Voice input через speech-to-text
- Планировщик задач (cron)
- Дешевле платных подписок

## Ограничения

- API-based: ограниченный функционал (нет прямого file editing)
- Бесплатные модели: лимиты и нестабильность
- Требует VPS (не в РФ)

## Связанные концепты

- [[memory_system_taxonomy|Memory System Taxonomy]] — разные типы памяти для AI
- [[llm_wiki|LLM Wiki]] — паттерн построения базы знаний

[[index|← Назад к индексу]]