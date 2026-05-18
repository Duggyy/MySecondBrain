---
title: Claude Code + Ollama = FULL LOCAL AI AGENT
type: source
tags: [local-ai, ollama, claude-code, privacy, offline-ai, qwen, open-source]
lang: en
created: 2026-05-18
source: https://www.youtube.com/watch?v=7kNz_6hKHVs
author: Prompt Engineer
---

## Summary

Tutorial на замену дорогих моделей Claude (Opus, Sonnet, Haiku) локальными моделями Ollama + Claude Code. Полностью бесплатный, приватный, работает локально на машине.

## Tech Stack

- **Ollama** — локальный runtime для LLM
- **Lightweight Models**: Qwen3.5:9b (рекомендуется для начала)
- **Claude Code** — интеграция с VS Code
- **VS Code + extensions** — IDE

## Key Benefits

✅ **Zero API costs** — никаких платежей за API  
✅ **100% Privacy** — всё запускается локально  
✅ **Open-source** — полный контроль над стеком  

## Setup Steps (Основное)

1. Установить Claude Code в VS Code
2. Выбрать модель Qwen 3.5 (beste для начинающих)
3. Установить Ollama (с фиксингом environment variables)
4. Скачать модель: `ollama pull qwen3.5:9b`
5. Настроить Claude Code для работы с локальной моделью
6. Тестирование базовых промптов

## Context Length Problem & Solution

**Problem**: Стандартные модели имеют ограниченный контекст (8192 токенов)  
**Solution**: Увеличить контекст через Modelfile:
- Создать 64K context версию
- Использовать её для больших проектов
- Balancing act между размером и скоростью

## Performance Metrics

На машине автора (8GB GPU, 16GB RAM):
- CPU usage: ~67%
- GPU usage: ~33%
- Скорость инференса: очень быстрая (реальное время разработки)

## Limitations

- Зависит от железа (8GB GPU минимум для Qwen3.5:9b)
- 64K контекст требует достаточно памяти
- Не замена для очень сложных задач

## Model Options by Hardware

- **8GB GPU**: Qwen3.5:9b (E4B effective 4 billion)
- **24GB GPU**: 21B или 26B модели
- **GPU 26GB+**: 31B модели (лучший выход, больше контекста)

## Alternative Pipelines

- LM Studio (вместо Ollama)
- Другие агенты (вместо Continue)
- RunPod (облачные GPUs если нет своего железа)

## Key Insight

Claude Code + Ollama = **агентское поведение на локальной машине**. Не просто запуск модели в cmd, а полноценный AI coding assistant с tool use, automatic context management и понимаием контекста.

## Related Topics for Wiki

- [[local_ai_deployment]] — новая страница
- [[ollama]] — инструмент
- [[qwen_models]] — модели
- [[privacy_first_ai]] — концепция
- [[claude_code]] — integration

[source: Claude Code + Ollama = FULL LOCAL AI AGENT.md]
