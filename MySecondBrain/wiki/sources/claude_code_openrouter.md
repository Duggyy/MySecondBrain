---
title: Claude Code + OpenRouter
type: source
tags: [claude-code, openrouter, free-access, deepseek, qwen]
lang: ru
created: 2026-04-21
sources: [Claude Code + OpenRouter.md]
---

# Claude Code + OpenRouter

## Ситуация
Claude Code требует подписку, но можно заменить модель на бесплатные через OpenRouter

## Решение
OpenRouter — единая точка доступа ко всем LLM. Claude Code поддерживает кастомные провайдеры.

## Установка
1. Node.js LTS + Git
2. `npm install -g @anthropic-ai/claude-code`
3. Регистрация на openrouter.ai → API ключ
4. Конфиг в `.claude_settings_local.json` проекта:
```json
{
  "options": { "openRouterApiKey": "your-key" },
  "models": { "default": "openrouter/deepseek-ai/deepseek-chat-v3-fresh" }
}
```

## Бесплатные модели
- DeepSeek V3
- Gemini Flash ($1.50/1M — в 10х дешевле Claude)
- Qwen 3.6 Plus Free

## Источник
JustAI, 2026-04-18
