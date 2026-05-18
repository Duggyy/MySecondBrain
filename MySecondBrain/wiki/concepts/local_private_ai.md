---
title: Local & Private AI Infrastructure
type: concept
tags: [local-ai, privacy, infrastructure, open-source, self-hosted]
lang: en
created: 2026-05-18
sources: [claude_code_ollama_local_agent, gemma4_local_ai_agent, claude_cowork_ollama_tailscale, private_ai_mobile]
---

## Определение

Запуск AI моделей полностью локально на собственном оборудовании — **вне зависимости от облачных сервисов**.

## Архитектура

### Layer 1: Model Runtime
- **Ollama** — простой runtime для LLM
- **MLX** — для Mac (Apple Silicon)
- **LM Studio** — альтернатива с UI

### Layer 2: Models
Легкие модели, которые работают локально:
- **Gemma 4 E4B** (4B параметров) — 9.6GB, работает на 8GB GPU
- **Qwen 3.5:9b** — 9B параметров, хороший balance
- **Larger variants** — 21B, 26B для большего контекста

### Layer 3: IDE/Editor
- **Claude Code** с локальной моделью
- **Continue IDE** (VS Code extension)
- **Other agents** (Cline, Copilot alternatives)

### Layer 4: Networking
- **Tailscale** — для secure remote access
- **ngrok** — для tunneling
- **Direct local network** — максимум приватности

## Key Benefits

### ✅ 100% Privacy
- Ничего не уходит в облако
- Все данные остаются на вашем устройстве
- Никакие сервисы не знают что вы делаете

### ✅ Zero API Costs
- Нет платежей за токены
- Нет limit'ов
- Используй сколько нужно

### ✅ Full Control
- Можешь customизировать модель
- Fine-tune под свои нужды
- Modify code directly

### ✅ Offline Capability
- Работает без интернета (после initial setup)
- Полная независимость от сервис-провайдеров

## Real Performance

Тесты показали:
- **Inference speed**: очень быстрая (real-time во время разработки)
- **Code generation quality**: Gemma 4 E4B достаточно хороша для:
  - Веб-разработки
  - Скриптования
  - Простых автоматизаций
- **Context window**: 8K по умолчанию, можно увеличить до 64K+ если памяти хватает

## Hardware Requirements

| GPU VRAM | Model | Size | Use Case |
|----------|-------|------|----------|
| 8GB | Gemma 4 E4B | 9.6GB | Light coding, basic apps |
| 24GB | Gemma 4 21B+ | 21GB+ | Medium projects |
| 26GB+ | Larger models | 31B+ | Complex projects |

**Alternatively**: RunPod — облачные дешевые GPUs если своего оборудования нет.

## Architecture Pattern: Claude Code + Ollama + Tailscale

**Local**: Claude Code + Gemma 4 на твоем ПК  
**Remote Access**: Tailscale VPN для работы из любого места  
**Setup**: 100% FREE & PRIVATE  

```
Your PC (Claude Code + Gemma 4)
        ↓ (Tailscale VPN)
    Remote Access
        ↓
    Any Location
```

## Use Cases

### 1. Development
Полноценный AI coding assistant без облака.

### 2. Privacy-sensitive Work
Например, работа с медиц. данными, legal docs, trade secrets.

### 3. Offline Environments
Места без интернета (например, удаленные серверы).

### 4. Cost Optimization
Если много токенов → local работает дешевле.

## Limiting Factors

- Производительность зависит от железа (GPU/CPU)
- Качество моделей ≈ облачным, но не всегда лучше
- Context window может быть меньше (зависит от памяти)
- Setup требует технических знаний

## Comparison: Local vs Cloud

| Aspect | Local | Cloud |
|--------|-------|-------|
| Privacy | 100% | Зависит от провайдера |
| Cost | Free (after hardware) | Per token |
| Speed | Fast (local) | Variable |
| Availability | Always (offline capable) | Depends on connection |
| Model quality | Good enough | Often better |
| Setup complexity | Medium | Easy |

## Future Trend

"Local AI" становится **standard**, не исключением:
- Apple: MLX для Mac
- Open source community: Ollama, LM Studio, LLaMA
- Users: постепенно мигрируют на local из-за privacy concerns

## Related

- [[claude_code_autonomous_agent]] — IDE layer
- [[free_access_methods]] — cost comparison
- [[infrastructure]] — deployment patterns
- [[privacy_first_ai]] — philosophy

[synthesized from: claude_code_ollama_local_agent, gemma4_local_ai_agent, claude_cowork_ollama_tailscale, private_ai_mobile]
