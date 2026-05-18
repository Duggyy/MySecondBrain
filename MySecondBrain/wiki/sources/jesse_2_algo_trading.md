---
title: Jesse 2.0 Is Here! Algo-trading reimagined
type: source
tags: [algo-trading, jesse-framework, backtesting, rule-significance, statistics]
lang: en
created: 2026-05-18
source: https://www.youtube.com/watch?v=Rw1zLZK3XJg
author: Algo-trading with Saleh
---

## Summary

Обзор Jesse 2.0 — major release алгоритмической торговой платформы. Главные обновления: переработанный UI, новые метрики backtesting и **Rule Significance Test** — статистический тест для определения predictive power entry-правила.

## Jesse: Что это?

Jesse — это фреймворк для алгоритмической торговли. Позволяет писать торговые стратегии, бэктестировать их, изучать метрики.

## Jesse 2.0: Основные Изменения

### 1. UI Redesign

**Старая версия**: navbar сверху  
**Новая версия**: sidebar с опцией minimize (экономит место на экране)

**Home Page**: теперь показывает:
- Недавние сессии backtesting
- Полезные статистики
- **CPU и RAM usage** — критично для production серверов

### 2. Новые Метрики Backtesting

**Existing**:
- Equity curve

**New**:
- Max underwater period
- Separate win rates for shorts and longs
- Log scale version equity curve
- Max drawdown chart (+ worst 5 periods)
- Underwater plot
- Monthly returns heat map
- Monthly returns distribution chart
- Trade panel distribution chart

Много из этих метрик раньше брались из QuantStats, теперь встроены в Jesse.

**Layout change**: Performance metrics теперь в sidebar (для удобства чтения).

### 3. Rule Significance Test (🎯 Главное)

**Что это**: Статистический тест, который определяет, **имеет ли entry-rule вашей стратегии predictive power**.

**Суть**:
- Берёт ваш entry-rule
- Симулирует случайные signals
- Сравнивает результаты
- Дает P-value (чем ниже, тем лучше)

**Threshold**: P-value < 10% = стратегия имеет edge  
P-value > 10% = нет edge (просто везение)

### 4. Пример: Стратегия БЕЗ Edge

**Стратегия**: 80% лонг, иногда шорт или ничего  
**Период**: крупный uptrend Bitcoin  
**Результат**: прибыль  
**Test результат**: P-value > 10% → **No edge**  
**Вывод**: стратегия работала только потому что был uptrend, не из-за её логики

### 5. Пример: Стратегия С Edge

**Результат**: P-value < 10% → **Has significance**  
**Chart**: actual returns лучше simulated ones  
**Period**: full year на lower timeframe (более точные симуляции)

## Technical Details

- **Entry rule analysis only** — не вся стратегия, только entry
- **Free version**: Rule Significance Test в research module (доступно всем)
- **Premium**: Dashboard версия (за подписку)
- **Backtest period matters**: Коротких периодов может быть недостаточно для точных результатов

## Key Insight

**Statistical rigor**: Jesse помогает отделить:
- Настоящий edge (predictive power)
- Везение (lucky market conditions)

Это критично для долгосрочного торговца.

## Related Topics for Wiki

- [[algo_trading]] — расширить
- [[jesse_framework]] — новая страница инструмента
- [[backtesting_methodology]] — статистический подход
- [[rule_significance]] — концепция
- [[statistical_edge]] — важная концепция

[source: Jesse 2.0 Is Here! Algo-trading reimagined.md]
