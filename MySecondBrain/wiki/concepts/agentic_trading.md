---
title: Agentic Trading Systems
type: concept
tags: [trading, ai-agents, automated-trading, institutional]
lang: en
created: 2026-05-18
sources: [alex_carter_agentic_trading_course, jesse_2_algo_trading, ai_premarket_research_automation]
---

## Определение

**Agentic Trading** = использование автономных AI-агентов для управления торговыми системами 24/7 без человеческого вмешательства.

## Архитектура (По Alex Carter)

### Module 0: Foundation
- Выживание в войне технологий (Silicon War)
- Основные концепции agentic систем

### Module 1-2: Core Stack
- Complete institutional-grade stack
- Architecture design patterns
- Workstation setup

### Module 3-7: Exchange Integration
- Claude + OpenRouter (LLM layer)
- WEEX, Alpaca, Interactive Brokers (execution)
- Multi-exchange support

### Module 8-11: Data & Intelligence
- WEEX Trading Assistant (автоматизация)
- Hyperliquid Whale Tracker (отслеживание больших участников)
- TradingView MCP (стратегии)
- Firecrawl MCP (web scraping для анализа)

### Module 12-14: Automation
- Daily Alpha Brief (генерирование идей)
- Claude Routines (24/7 процессы)
- Pine Script разработка

### Module 15-19: Advanced Systems
- Telegram интеграция (уведомления)
- TradingView x WEEX Webhook (real-time)
- Prediction Markets
- Monitoring (Agent PNL, Senpi)

### Module 20-25: Agentic Execution
- **Hermes** — агент для задач
- **OpenClaw** — специализированный агент
- Комбинация Hermes + OpenClaw для полной автоматизации
- Python Trading Bot scaffolding
- VPS deployment на Hostinger
- Live operations dashboard

## Key Innovations

### 1. Institutional-Grade System
Не просто один инструмент, а полностью интегрированная система как у хедж-фондов:
- Data pipeline
- Research layer
- Execution layer
- Monitoring layer

### 2. Multi-Exchange
- Одна система управляет несколькими биржами
- Arbitrage opportunities
- Risk management across platforms

### 3. Whale Tracking
- Отслеживание больших позиций
- Понимание рыночной динамики
- Early signals

### 4. MCP Protocol Integration
Model Context Protocol позволяет Claude работать с:
- TradingView стратегиями напрямую
- Реальными данными через API
- Custom tools и интеграции

## Statistical Rigor (Jesse 2.0)

### Rule Significance Test
Не все "прибыльные" стратегии имеют edge:
- Многие работают только из-за везения (lucky market conditions)
- Rule Significance Test определяет наличие real predictive power
- **P-value < 10%** = стратегия имеет edge
- **P-value > 10%** = нет edge (просто noise)

### Backtesting Metrics
- Max underwater period
- Separate win rates (shorts vs longs)
- Monthly returns distribution
- Trade distribution analysis

## Mindset Shift

**От**: "Я предсказываю рынок"  
**К**: "Я строю систему, которая находит статистические края"

**От**: Manual trading  
**К**: Agentic 24/7 execution

**От**: Индивидуальные инструменты  
**К**: Institutional-grade stack

## Key Insight: Operational Edge

Alex Carter ссылается на SMB Capital: **The real edge is operational**

> "Not prediction. The real edge is operational. How quickly you prepare, how clean your process is, and how effectively you can execute."

Это означает:
- ✅ Speed of information processing
- ✅ Cleanliness of execution
- ✅ Risk management efficiency
- ✅ Automation of repetitive tasks

Агенты excel в этом.

## Related

- [[claude_code_autonomous_agent]] — underlying technology
- [[ai_in_trading]] — broader context
- [[free_access_methods]] — cost optimization
- [[infrastructure]] — deployment

[synthesized from: alex_carter_agentic_trading_course, jesse_2_algo_trading, ai_premarket_research_automation]
