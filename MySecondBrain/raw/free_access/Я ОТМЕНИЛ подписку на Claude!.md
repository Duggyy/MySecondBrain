# Я ОТМЕНИЛ подписку на Claude! Как получить Opus 4.5 БЕСПЛАТНО (Antigravity auth)

## Ситуация/Проблема
- Google блокирует доступ к AntiGravity
- Лимиты на Opus и Sonnet вылетают через 30 минут работы
- Нужен способ получить доступ к топовым моделям Claude бесплатно

## Решение
Vibe Proxy / CLIProxyAPIPlus — локальный прокси, который перехватывает запросы от редактора кода и перенаправляет через подписочный аккаунт (AntiGravity/Claude/GitHub Copilot и др.)

```
Вы → VibeProxy → AntiGravity → Claude Opus/Sonnet → Ответ
```

## Бесплатные модели через OpenRouter
1. Зарегистрироваться на openrouter.ai (бесплатно, без привязки карты)
2. Создать API ключ
3. Установить Claude Code: `npm install -g @anthropic-ai/claude-code`
4. Создать файл `~/.claude_settings_local.json` с настройками прокси
5. Выбрать бесплатную модель (Qwen 3.6 Plus Free)

## Команды для подключения
| Команда | Модель | Описание |
|---------|--------|----------|
| `opus` | Claude Opus 4.5 | Самая умная — для сложных задач |
| `sonnet` | Claude Sonnet 4.5 | Быстрая и умная |
| `sonnet-no` | Claude Sonnet 4.5 | Без размышлений — максимальная скорость |
| `g3` | Gemini 3 Pro | Для работы с картинками |

## Windows (CLIProxyAPIPlus)
1. Скачать с github.com/router-for-me/CLIProxyAPIPlus/releases
2. Распаковать в `C:\CLIProxyAPIPlus\`
3. Переименовать `config.example.yaml` в `config.yaml`
4. Закомментировать секцию `api-keys:`
5. Запустить: `.\CLIProxyAPIPlus.exe --antigravity-login`
6. Авторизоваться через Google
7. Запустить прокси: `.\CLIProxyAPIPlus.exe`
8. Создать BAT-файлы для быстрого запуска с нужной моделью

## Источники
- YouTube: https://www.youtube.com/watch?v=blg4YYJF2Vw (Дрессировщик Нейросетей)
- Дата: 2026-01-10
