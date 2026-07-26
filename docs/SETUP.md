# Setup Guide

## 1. Upload to GitHub

Create a new public repository named:

```text
concierge-os-n8n
```

Upload all files and folders from this package.

Do not upload the ZIP file itself. Extract it first, then upload the contents.

## 2. Import Workflows into n8n

In n8n:

1. Open **Workflows**
2. Select **Import from URL**
3. Paste one raw GitHub JSON URL
4. Save the imported workflow
5. Repeat for all workflow files

See `N8N-IMPORT-URLS.md`.

## 3. Credentials

Create and connect:

- Telegram Bot credential
- Google Calendar OAuth2 credential
- OpenAI API credential

After import, open every node showing a credential warning and select the correct credential.

## 4. Telegram

1. Create a Telegram bot using BotFather.
2. Add the bot token to n8n.
3. Start a chat with your bot.
4. Retrieve your Telegram Chat ID.
5. Replace `$env.TELEGRAM_CHAT_ID` if environment variables are unavailable.

## 5. OpenAI

The current workflow calls:

```text
POST https://api.openai.com/v1/responses
```

Default model:

```text
gpt-5-mini
```

You can replace this in the HTTP Request node or set:

```text
OPENAI_MODEL
```

## 6. Google Calendar

Connect the Google Calendar OAuth2 credential and ensure the workflow uses the primary calendar.

Workflow timezone:

```text
Asia/Dubai
```

## 7. Test

Test in this order:

1. Opportunity Scoring
2. Main Orchestrator
3. Daily Brief
4. Weekly Planner

Send this Telegram message:

```text
Bu akşam ne yapayım?
```

The bot should read the next seven days of calendar availability and reply in Turkish.

## 8. Activate

Activate workflows only after successful manual tests.

Scheduled workflows:

- Daily Brief: every day at 08:00
- Weekly Planner: Sunday at 17:00
