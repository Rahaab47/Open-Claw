# OpenClaw with General Agents

This repository contains the agent orchestration configuration for operating **OpenClaw** — the AI gateway that connects language models to messaging channels.

## What's here

- **AGENTS.md** — Operations reference for AI agents. Covers install, config, channels (WhatsApp, Telegram, Discord), memory, skills, plugins, MCP, automation, and security for OpenClaw.
- **CLAUDE.md** — Import marker that loads `AGENTS.md` into the agent's context.

## Quick start

1. Install OpenClaw: `iwr -useb https://openclaw.ai/install.ps1 | iex` (Windows)
2. Set your API key: `$env:GEMINI_API_KEY="your-key"`
3. Onboard: `openclaw onboard --flow quickstart --non-interactive --json --accept-risk --auth-choice gemini-api-key --secret-input-mode ref`
4. Override model: `openclaw config set agents.defaults.model.primary "openai/gpt-5.4-mini"`
5. Launch dashboard: `openclaw dashboard`
6. Add channels: `openclaw channels login --channel whatsapp`

## Requirements

- OpenClaw ≥ v2026.5.7
- Node.js ≥ 22.16
- A Gemini or OpenAI API key (free tier)
