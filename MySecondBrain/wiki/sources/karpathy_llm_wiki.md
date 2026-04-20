---
title: "LLM Wiki — Karpathy's Pattern"
type: source
tags: [knowledge-management, karpathy, llm-wiki, pattern]
lang: en
created: 2026-04-20
source_file: raw/knowledge_base/KARPATHY-llm-wiki.md
---

## Описание

Авторский паттерн Andre Karpathy для построения персональных баз знаний с помощью LLM. Оригинальный gist: karpathy/442a6bf555914893e9891c11519de94f

## Ключевые идеи

- **Накопление vs RAG**: вместо поиска по сырым документам — инкрементальное построение постоянной wiki
- **Три слоя**: Raw Sources → Wiki → Schema (CLAUDE.md)
- **LLM делает бухгалтерию**: обновляет перекрестные ссылки, синхронизирует резюме, помечает противоречия

## Архитектура

| Слой | Описание |
|------|----------|
| Raw sources | Неизменяемые исходные документы |
| Wiki | LLM-генеренные markdown-страницы |
| Schema | Инструкции для LLM (CLAUDE.md) |

## Операции

1. **Ingest** — обработка нового источника
2. **Query** — ответы с цитированием wiki
3. **Lint** — проверка здоровья wiki

## Применено в этом проекте

Этот проект построен по методу LLM Wiki. Данный документ — один из первичных источников, описывающих методологию.

## Связанные источники

- [[Claude Code + Karpathy's Obsidian]] — практическая реализация
- [[Telegram + Claude Code база знаний]] — использование Telegram как источника

[[index|← Назад к индексу]]