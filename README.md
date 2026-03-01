# telegram-transcribe

Telegram bot that transcribes voice and audio messages using OpenAI's `gpt-4o-transcribe` model. Language is auto-detected.

Only messages from allowed user IDs are processed. Everything else is silently ignored.

## Environment variables

| Variable | Description |
|---|---|
| `TELEGRAM_BOT_TOKEN` | Bot token from [@BotFather](https://t.me/BotFather) |
| `OPENAI_API_KEY` | OpenAI API key |
| `ALLOWED_USER_IDS` | Comma-separated list of Telegram user IDs |

## Run with Docker

```bash
docker run -d --name telegram-transcribe \
  -e TELEGRAM_BOT_TOKEN=... \
  -e OPENAI_API_KEY=... \
  -e ALLOWED_USER_IDS=123,456 \
  ghcr.io/gofort/telegram-transcribe:latest
```
