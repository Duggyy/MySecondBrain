---
title: I Built a Local AI Agent with Gemma 4 — Runs Fully Offline
type: source
tags: [local-ai, gemma, offline-ai, continue-ide, privacy, coding-agent, open-source]
lang: en
created: 2026-05-18
source: https://www.youtube.com/watch?v=VhjshBCqwrQ
author: Prompt Engineer
---

## Summary

Полный гайд по настройке локального AI-агента с Gemma 4 (4B модель) на собственной машине без подключения к интернету. Демонстрирует создание веб-приложений в режиме оффлайна с использованием Continue IDE + Ollama.

## Tech Stack

- **Gemma 4 E4B** (Effective 4 Billion) — модель Google, очень легкая
- **Ollama** — локальный LLM runtime
- **Continue IDE** — open-source AI coding agent для VS Code
- **VS Code** — редактор

## System Requirements for Demo

- 8GB GPU
- 16GB RAM (minimum)
- Model size: 9.6GB

## Setup Process

### 1. Install VS Code + Continue Extension
```
Extensions → Continue (open-source AI code agent)
```

### 2. Install Ollama
```bash
ollama pull gemma4:e4b
```

### 3. Configure Continue
- Settings → Models → Add Ollama provider
- Auto-detect: configure with Ollama provider
- Model format:
  ```
  title: Gemma 4 E4B
  model: gemma4:e4b
  provider: ollama
  ```

### 4. Configure Tools (MCP servers)
- 14 built-in tools available
- Can add custom MCP servers
- Tool execution: ask-first, automatic, or exclude

## Performance Demonstration

**Task**: Create login page with dark theme  
**Metrics**:
- CPU usage: 67%
- GPU usage: 32-33%
- Inference speed: **very fast** (не замедленное видео)
- Context window: 8192 tokens
- Full web app: Create + style in real-time

## Key Capabilities Shown

✅ **Agentic behavior** — понимает контекст, автоматически обновляет  
✅ **Tool use** — использует терминал, файловую систему  
✅ **Code generation** — HTML + CSS в реальном времени  
✅ **Iterative improvement** — принимает изменения на ходу  

## Context Management

Important for local models:
- Limited context window (8192 tokens here)
- Can request summarization of previous work
- Continue handles context tracking

## Hardware Scaling

| GPU VRAM | Model | Size | Context |
|----------|-------|------|---------|
| 8GB | Gemma 4 E4B | 9.6GB | 8K |
| 24GB | Gemma 4 variants | 21B, 26B | Higher |
| 26GB+ | Larger models | 31B+ | 32K+ |

## Surprising Finding

**Year-over-year improvement is dramatic**. Gemma 4 is so much more capable than models from 1 year ago. Good enough for basic automation and web design tasks.

## Comparison of Agents

Continue vs Claude Code vs Copilot vs Cline — all have different strengths.

## Full Architecture

```
Ollama (port 11434)
    ↓
Gemma 4 E4B model
    ↓
Continue IDE (VS Code extension)
    ↓
Developer/User
```

Continue sends commands to Ollama port, gets responses, handles agent behavior (tool use, context management).

## Alternative Tools

Instead of:
- Ollama → LM Studio
- Continue → other agents
- Model → other local models

## Related Topics for Wiki

- [[gemma_models]] — модели Google
- [[local_coding_agents]] — категория
- [[continue_ide]] — инструмент
- [[agentic_ai]] — концепция
- [[offline_ai]] — тренд

[source: I Built a Local AI Agent with Gemma 4 — Runs Fully Offline.md]
