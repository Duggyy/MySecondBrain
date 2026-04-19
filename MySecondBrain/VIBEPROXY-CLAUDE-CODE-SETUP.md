# Как использовать Claude Code с моделями Opus и Sonnet через Antigravity

Инструкция для тех, кто хочет использовать Claude Code с мощными моделями Claude Opus и Sonnet практически бесплатно.

---

## Что это и как работает?

**VibeProxy** — бесплатная программа, которая позволяет использовать разные AI-подписки с Claude Code:
- **Antigravity** — даёт доступ к Claude Opus 4.5 и Sonnet 4.5 (наш основной вариант)
- Claude Pro/Max — если у вас есть подписка на claude.ai
- ChatGPT Plus/Pro — для моделей GPT
- И другие

**В этой инструкции мы используем Antigravity** — это подписка через Google аккаунт, которая даёт доступ к моделям Claude Opus и Sonnet. По сути — получаем мощные модели Claude практически бесплатно.

**Как это работает:**
```
Вы вводите команду → VibeProxy → Antigravity → Claude Opus/Sonnet → Ответ
```

---

## Что нужно

- **Mac с чипом Apple (M1, M2, M3, M4)** — Intel Mac не поддерживается
- **macOS 13 или новее** (Ventura, Sonoma, Sequoia)
- **Google аккаунт** — для авторизации в Antigravity
- **Node.js** — для установки Claude Code

---

## Установка (шаг за шагом)

### Шаг 1: Установите Node.js (если ещё нет)

Откройте программу **Терминал** (Cmd+Пробел → введите "Terminal").

Введите команду:
```bash
brew install node
```

> Если brew не установлен:
> ```bash
> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
> ```

### Шаг 2: Установите Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

### Шаг 3: Скачайте и установите VibeProxy

1. Перейдите: **https://github.com/automazeio/vibeproxy/releases**
2. Скачайте **VibeProxy.zip** (самый свежий)
3. Распакуйте и перетащите **VibeProxy.app** в папку **Программы**
4. Запустите VibeProxy

> Если Mac блокирует: правая кнопка → "Открыть" → "Открыть"

### Шаг 4: Подключите Antigravity

1. Кликните на иконку VibeProxy в верхней панели Mac
2. Выберите **Open Settings**
3. Найдите **Antigravity** и нажмите **Connect**
4. Войдите через свой **Google аккаунт**
5. После входа должно показать **Connected**

### Шаг 5: Настройте команды

Откройте терминал и введите:
```bash
open ~/.zshrc
```

Добавьте в конец файла:

```bash
# ========================================
# Claude Code через Antigravity
# ========================================

# Opus — самая мощная модель
opus() {
  exec env ANTHROPIC_BASE_URL="http://localhost:8317" \
    ANTHROPIC_API_KEY="sk-vibeproxy-dummy" \
    ANTHROPIC_MODEL="gemini-claude-opus-4-5-thinking" \
    claude
}

# Sonnet — быстрая умная модель
sonnet() {
  exec env ANTHROPIC_BASE_URL="http://localhost:8317" \
    ANTHROPIC_API_KEY="sk-vibeproxy-dummy" \
    ANTHROPIC_MODEL="gemini-claude-sonnet-4-5-thinking" \
    claude
}

# Sonnet без "размышлений" — ещё быстрее
sonnet-no() {
  exec env ANTHROPIC_BASE_URL="http://localhost:8317" \
    ANTHROPIC_API_KEY="sk-vibeproxy-dummy" \
    ANTHROPIC_MODEL="gemini-claude-sonnet-4-5" \
    claude
}

# Gemini 3 Pro — работает с картинками
g3() {
  exec env ANTHROPIC_BASE_URL="http://localhost:8317" \
    ANTHROPIC_API_KEY="sk-vibeproxy-dummy" \
    ANTHROPIC_MODEL="gemini-3-pro-image-preview" \
    claude
}
```

Сохраните (Cmd+S) и выполните:
```bash
source ~/.zshrc
```

---

## Как пользоваться

Откройте терминал и введите одну из команд:

| Команда     | Модель            | Описание                                  |
| ----------- | ----------------- | ----------------------------------------- |
| `opus`      | Claude Opus 4.5   | Самая умная модель — для сложных задач    |
| `sonnet`    | Claude Sonnet 4.5 | Быстрая и умная — для обычной работы      |
| `sonnet-no` | Claude Sonnet 4.5 | Без "размышлений" — максимальная скорость |
| `g3`        | Gemini 3 Pro      | Для работы с картинками                   |

**Пример:**
```bash
opus
```

---

## Какую модель выбрать?

**Для обычной работы:** `sonnet`
Быстрый, справляется с большинством задач.

**Для сложных задач:** `opus`
Самая мощная модель. Архитектура, сложная отладка, анализ большого проекта.

**Когда важна скорость:** `sonnet-no`
Отвечает быстрее, но менее глубоко.


---

## Какие модели даёт Antigravity

Через подписку Antigravity доступны:

| Модель | Описание |
|--------|----------|
| Claude Opus 4.5 | Самая мощная модель Claude (с thinking) |
| Claude Sonnet 4.5 | Быстрая модель Claude (с thinking и без) |
| Gemini 3 Pro | Модель Google с поддержкой изображений |

**Важно:** Модели через Antigravity работают с автоматическим режимом "thinking" (размышления). Вы не можете менять глубину thinking — это контролируется сервером.

---

## Другие подписки (если есть)

VibeProxy также поддерживает:

- **Claude Pro/Max** — если у вас есть подписка claude.ai
- **ChatGPT Plus/Pro** — для моделей GPT-5
- **Gemini CLI** — через Google Cloud

Но для большинства задач **Antigravity достаточно** — вы получаете доступ к топовым моделям Claude.

---

## Если что-то не работает

### "Connection refused"
VibeProxy не запущен. Откройте его из папки Программы.

### "Rate limit" или "Quota exceeded"
Подождите немного — исчерпан лимит запросов.

### "Unauthorized"
Переподключите Antigravity:
1. VibeProxy → Settings
2. Antigravity → Disconnect
3. Antigravity → Connect (войдите заново)

### Проверить работу VibeProxy
```bash
curl http://localhost:8317/v1/models
```

---

## Для Windows

VibeProxy работает только на Mac с чипом Apple.

Для Windows нужен **CLIProxyAPI** — настройка сложнее, требуется техническая подготовка.

---

## Важно

- **VibeProxy должен быть запущен** перед использованием команд
- **Все данные остаются локально** — безопасно
- **Antigravity использует ваш Google аккаунт** — авторизация через него

---

*Если есть вопросы — спрашивайте!*
