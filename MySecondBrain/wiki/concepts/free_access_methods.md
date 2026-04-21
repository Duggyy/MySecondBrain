---
title: "Свободный доступ к AI-моделям"
type: concept
tags: [free-access, claude-code, gemini, openrouter, antigravity]
lang: ru
sources: [gemini_cli_tutorial.md, cliclaw_tutorial.md, vibe_proxy_tutorial.md, claude_routines.md, claude_code_openrouter.md, otmenil_podpisku_na_claude.md]
created: 2026-04-20
---

## Концепция

Обзор методов бесплатного или условно-бесплатного доступа к топовым AI-LLM моделям. Особенно актуально для пользователей из РФ, где многие сервисы ограничены.

## Методы доступа

### Полностью бесплатные

| Метод | Модели | Лимиты | Примечание |
|-------|--------|--------|------------|
| **Gemini CLI** | Gemini 2.0, 3.1 | 1000 req/day | 2M token context |
| **OpenRouter** | Меняются | Варьируется | Требует проверки free-tier моделей |
| **CliClaw** | Claude/Codex/Gemini | Зависит от модели | Telegram-интерфейс |

### Условно-бесплатные (через прокси)

| Метод | Требования | Модели |
|-------|-----------|--------|
| **Vibe Proxy** | AntiGravity аккаунт | Opus 4.5, Sonnet 4.5 |
| **CLIProxyAPIPlus** | AntiGravity аккаунт | Opus 4.5, Sonnet 4.5 |
| **Antigravity auth** | Google аккаунт | Sonnet, Opus |

### Платные прокси

| Сервис | Цена | Примечание |
|--------|------|------------|
| Claude Code | $20+/месяц | Официальный клиент |
| OpenRouter | Pay-per-use | Гибкие лимиты |

## Сравнение контекстных окон

| Модель | Context Window |
|--------|---------------|
| Gemini CLI | 2,000,000 tokens |
| Claude Code | 200,000 tokens |
| GPT-4o | 128,000 tokens |

## Географические ограничения

Многие сервисы (AntiGravity, Claude.ai) блокируют пользователей из РФ. Обходные решения:
- VPS за пределами РФ
- Прокси-сервисы
- Локальные прокси (Vibe Proxy)

## Риски и ограничения

1. **Нестабильность** — бесплатные модели меняются
2. **Лимиты** — быстро вылетают при интенсивном использовании
3. **Блокировки** — аккаунты могут быть забанены
4. **Токены** — даже "бесплатные" методы требуют API keys

## Связанные концепты

- [[telegram_ai_agents|Telegram AI Agents]] — архитектура AI-агентов на VPS
- [[memory_system_taxonomy|Memory System Taxonomy]] — управление памятью

[[index|← Назад к индексу]]