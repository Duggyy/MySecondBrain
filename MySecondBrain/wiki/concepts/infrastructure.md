---
title: "Инфраструктура AI"
type: concept
tags: [infrastructure, vps, vpn, security, server]
lang: ru
created: 2026-04-20
---

## Обзор

Инфраструктура для работы с AI: VPS-серверы, VPN, прокси, безопасность.

## Ключевые компоненты

### VPS (Virtual Private Server)

- **Цена**: ~$1-5/месяц
- **Расположение**: Европа/США (не РФ для AI)
- **ОС**: Ubuntu 22.04/24.04
- **Использование**: VPN, AI-агенты, боты, хостинг

### VPN протоколы

| Протокол | Устойчивость | Маскировка |
|----------|--------------|------------|
| VLESS Reality | Высокая | Да |
| Amnesia | Высокая | Да |
| Hysteria 2 | Высокая | Да |

### Безопасность сервера

- SSH-ключи вместо паролей
- Firewall (UFW)
- Fail2Ban (защита от брутфорса)
- Регулярные обновления

## AI-агенты на сервере

См. [[telegram_ai_agents|Telegram AI Agents]] — агенты типа CliClaw, QwenClaw

## Связанные источники

- [[vpn_setup_with_claude_code|VPN Setup with Claude Code]]

[[index|← Назад к индексу]]