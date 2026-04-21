# Claude Code НАВСЕГДА бесплатно (OpenRouter)

## Ситуация/Проблема
Claude Code требует подписку ($20-200/месяц), но можно заменить базовую модель на бесплатные альтернативы через OpenRouter

## Решение
OpenRouter — единая точка доступа ко всем LLM моделям. Claude Code поддерживает кастомные провайдеры.

## Установка
1. Установить Node.js (LTS) с nodejs.org
2. Установить Git с git-scm.com
3. Установить Claude Code: `npm install -g @anthropic-ai/claude-code`
4. Зарегистрироваться на openrouter.ai
5. Создать API ключ в разделе API Keys
6. В папке проекта создать/отредактировать `.claude_settings_local.json`

## Конфигурация
```json
{
  "options": {
    "openRouterApiKey": "your-key-here"
  },
  "models": {
    "default": "openrouter/deepseek-ai/deepseek-chat-v3-fresh"
  }
}
```

## Бесплатные модели OpenRouter
- DeepSeek V3 — для большинства задач
- Gemini Flash — $1.50/1M токенов (vs $15 для Claude Opus)
- Qwen 3.6 Plus Free — бесплатная

## Почему платные модели иногда лучше
Gemma 4 (Google) стоит $0.14/1M токенов — в 20 раз дешевле Claude Sonnet, при этом качество сопоставимо для большинства задач.

## Подключение Telegram
Claude Code можно подключить к Telegram через специальный мост.

## Источники
- YouTube: https://www.youtube.com/watch?v=dTOehd838tk (JustAI)
- Дата: 2026-04-18
