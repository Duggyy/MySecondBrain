---
title: "Бесплатный Claude Opus через Vibe Proxy"
type: source
tags: [free, claude, opus, sonnet, antigravity, proxy, vibe-proxy]
lang: ru
created: 2026-04-18
source_file: raw/free_access/Я ОТМЕНИЛ подписку на Claude! Как получить Opus 4.5 БЕСПЛАТНО (Antigravity auth).md
author: Дрессировщик Нейросетей
published: 2026-01-10
source_url: "https://www.youtube.com/watch?v=blg4YYJF2Vw"
---

## Описание

Обход ограничений AntiGravity с помощью локального прокси (Vibe Proxy / CLIProxyAPIPlus). Позволяет получить доступ к Claude Opus и Sonnet бесплатно через уже существующие подписки.

## Инструменты

| Инструмент | Платформа | Описание |
|------------|-----------|----------|
| **Vibe Proxy** | Mac | GUI-приложение, красивый интерфейс |
| **CLIProxyAPIPlus** | Windows/Linux | Терминальный, кроссплатформенный |

## Как работает

```
Editor → Local Proxy (localhost:8317) → AntiGravity subscription → Cloud API
```

Vibe Proxy — локальный прокси, который:
1. Перехватывает запросы от редактора
2. Использует существующую подписку (AntiGravity, Claude, Gemini и т.д.)
3. Прокидывает запросы в облако

## Настройка (Mac)

1. Установить Vibe Proxy
2. Подключить аккаунты AntiGravity/Gemini/Claude
3. Добавить записи в `~/.zshrc`:

```bash
export http_proxy=http://localhost:8317
export https_proxy=http://localhost:8317
```

## Доступные модели через AntiGravity

- **Claude Opus 4.5** (thinking) — топовая модель
- **Claude Sonnet 4.5** (thinking)
- **Claude Sonnet 4.5** (без размышлений)
- **Gemini Pro**

## Преимущества

- Бесплатный доступ к топовым моделям
- Обход блокировок Google
- Экономия на подписках (несколько аккаунтов = больше лимитов)
- Работает с Cursor, VS Code (Cline), Claude Code

## Ограничения

- Mac: Vibe Proxy (GUI)
- Windows/Linux: CLIProxyAPIPlus (терминал)
- Нужен аккаунт AntiGravity или аналогичного сервиса

## Связанные инструменты

- [[cliclaw_tutorial|CliClaw]] — Telegram-агент
- [[gemini_cli_tutorial|Gemini CLI]] — бесплатный CLI-ассистент

[[index|← Назад к индексу]]