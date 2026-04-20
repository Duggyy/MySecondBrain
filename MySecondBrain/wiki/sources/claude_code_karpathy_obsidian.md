---
title: "Claude Code + Karpathy's Obsidian = New Meta"
type: source
tags: [claude-code, obsidian, memory-system, karpathy, pinecone]
lang: en
created: 2026-04-18
source_file: raw/knowledge_base/Claude Code + Karpathy's Obsidian = New Meta.md
author: Jack Roberts
published: 2026-04-10
source_url: "https://www.youtube.com/watch?v=eglVxLaWRUU"
---

## Описание

Практический гайд по настройке Obsidian memory system для Claude Code на основе метода Andre Karpathy. Автор — Jack Roberts (AI automation entrepreneur).

## Ключевые концепции

### Три слоя архитектуры памяти

| Слой | Назначение | Пример |
|------|-----------|--------|
| CLAUDE.md | Identity — кто я, правила, инструкции | "Я — персональный ассистент" |
| Obsidian | Reasoning — активные проекты, структура | "Как я думаю" |
| Pinecone | Warehouse — архивы, транскрипты | "Что я говорил" |

### Ограничения чистого Obsidian RAG

1. **Token tax** — CLAUDE.md и index.md растут линейно с размером wiki
2. **Нет семантического поиска** — работает по темам, не по смыслу
3. **Staleness (drift)** — резюме устаревают
4. **Не масштабируется** — ~100 файлов ОК, 10,000 — проблема

### Когда что использовать

- **Obsidian**: активные проекты, decision logs, idea gardens — где важна структура и связи
- **Pinecone**: транскрипты, исследования, книги — где важна точность
- **NotebookLM**: глубокие исследования, анализ 200+ ресурсов

## Процесс настройки

1. Скачать Obsidian
2. Создать vault (папку)
3. Скопировать KARPATHY-llm-wiki.md в raw/
4. Запустить Claude Code в папке
5. Дать промпт: "создай структуру по приложенной схеме"
6. Настроить Obsidian Web Clipper для сохранения статей
7. Дропать источники, Claude обновляет 10-15 страниц за раз

## Связи

- Описывает реализацию паттерна [[karpathy_llm_wiki|LLM Wiki]]
- Автор: [[jack_roberts|Jack Roberts]]

[[index|← Назад к индексу]]