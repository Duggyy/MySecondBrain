---
title: "Memory System Taxonomy"
type: concept
tags: [memory, claude-code, obsidian, pinecone, architecture]
lang: en
created: 2026-04-20
---

## Концепция

Разные системы памяти имеют разную "физику" — подходят для разных задач. Author: [[jack_roberts|Jack Roberts]].

## Три слоя персональной памяти

### 1. CLAUDE.md = Identity

- Кто я
- Мои правила
- Инструкции
- Никогда не меняется в середине сессии

### 2. Obsidian = Reasoning

- Активные проекты
- Decision logs
- Idea gardens
- **Важно**: структура и связи между идеями имеют значение
- Ключевое слово: **reasoning**, не memory

### 3. Pinecone = Warehouse

- Архивы
- Транскрипты YouTube
- Книги
- Полная история переписки
- Ключевое слово: **exact recall**

## Аналогия

| Система | Аналогия |
|---------|----------|
| CLAUDE.md | My badge — кто я |
| Obsidian | My workshop — как я думаю |
| Pinecone | My warehouse — что я говорил |

## Ограничения Obsidian-only систем

1. **Token tax** — CLAUDE.md и index.md растут линейно
2. **Нет семантики** — работает по заголовкам, не по смыслу
3. **Drift** — резюме устаревают
4. **Плохо масштабируется** — 100 файлов ОК, 10,000 — дорого

## Практическое правило

- **Obsidian**: то, что меняется, где важны связи
- **Pinecone**: то, что не меняется, где важна точность

## Связанные концепты

- [[llm_wiki|LLM Wiki]] — базовый паттерн
- [[claude_code_karpathy_obsidian|Claude Code + Karpathy's Obsidian]] — практическая реализация

[[index|← Назад к индексу]]