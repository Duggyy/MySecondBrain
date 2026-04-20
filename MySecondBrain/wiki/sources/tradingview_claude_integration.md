---
title: "Claude Code + TradingView Integration"
type: source
tags: [trading, tradingview, claude-code, mcp, automated-trading]
lang: ru
created: 2026-04-20
source_file: raw/trading/Как подключить Claude Code к TradingView (это меняет правила игры).md
author: АРДЕНСКИЙ | Трейдинг и психология
published: 2026-04-20
source_url: "https://www.youtube.com/watch?v=2LvuxpXNNw8"
---

## Описание

Подключение Claude Code к TradingView через MCP-сервер. Полноценный агент, который видит графики в реальном времени, управляет алёртами, пишет и тестирует стратегии на Pine Script.

## Что умеет Claude Code с TradingView

- **Реальное время видение графиков** — видит свечи, индикаторы, инструменты рисования
- **Управление алёртами** — создание, удаление, редактирование
- **Мониторинг чартов** — реалтайм наблюдение
- **Написание Pine Script стратегий** — сам пишет и тестирует
- **Поиск лучших метрик** — автоматическая оптимизация

## Архитектура

```
TradingView Desktop → MCP Server → Claude Code → Trading decisions
```

## Требования

| Компонент | Требование |
|-----------|------------|
| Claude Code | Платная подписка ($20+/месяц) |
| TradingView | Желательно Premium |
| VPN | Не из РФ |
| VPS/API | Для автоматизации |

## Настройка (кратко)

1. Установить Git, Node.js
2. Установить Claude Code CLI
3. Настроить TradingView Desktop
4. Подключить MCP-сервер для TradingView
5. Настроить авторизацию

## Связанные инструменты

- [[bitget_trading_tutorial|BitGet Trading MCP]] — автоматизация торговли через BitGet
- [[trading_indicators_tutorial|AI Trading Indicators]] — AI для анализа индикаторов

[[index|← Назад к индексу]]