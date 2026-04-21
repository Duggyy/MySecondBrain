# Я ОТМЕНИЛ подписку на Claude!

## Ситуация
- Google блокирует доступ к AntiGravity
- Лимиты на Opus и Sonnet вылетают через 30 минут
- Нужен способ получить Claude Opus/Sonnet бесплатно

## Решение
Vibe Proxy / CLIProxyAPIPlus — локальный прокси для перенаправления через подписку AntiGravity

## Команды (Mac)
```bash
# ~/.zshrc
opus() {
  exec env ANTHROPIC_BASE_URL="http://localhost:8317" \
    ANTHROPIC_API_KEY="sk-vibeproxy-dummy" \
    ANTHROPIC_MODEL="gemini-claude-opus-4-5-thinking" \
    claude
}
sonnet() {
  exec env ANTHROPIC_BASE_URL="http://localhost:8317" \
    ANTHROPIC_API_KEY="sk-vibeproxy-dummy" \
    ANTHROPIC_MODEL="gemini-claude-sonnet-4-5-thinking" \
    claude
}
```

## Windows (CLIProxyAPIPlus)
1. Скачать с github.com/router-for-me/CLIProxyAPIPlus/releases
2. Переименовать config.example.yaml → config.yaml
3. Закомментировать секцию api-keys:
4. `.\CLIProxyAPIPlus.exe --antigravity-login`
5. Запустить: `.\CLIProxyAPIPlus.exe`

## Источник
- Дрессировщик Нейросетей, 2026-01-10
