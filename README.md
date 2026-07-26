# Concierge OS for n8n

Concierge OS is a modular personal AI Chief of Staff designed for Savaş in Dubai.

It helps with:

- Daily and weekly planning
- Google Calendar awareness
- Fitness and boxing consistency
- Social and networking opportunities
- Style and grooming
- Social confidence and respectful approaches
- Travel and weekend planning
- Career, learning and finance routines

## Repository Structure

```text
concierge-os-n8n/
├── workflows/
│   ├── 01-concierge-main-orchestrator.json
│   ├── 02-concierge-daily-brief.json
│   ├── 03-concierge-weekly-planner.json
│   └── 04-concierge-opportunity-scoring.json
├── docs/
│   ├── SETUP.md
│   ├── N8N-IMPORT-URLS.md
│   └── ROADMAP.md
├── prompts/
│   └── concierge-orchestrator-prompt.md
├── templates/
│   └── user-profile-template.csv
├── .gitignore
├── LICENSE
└── README.md
```

## Quick Start

1. Upload this repository to GitHub.
2. Keep the repository public if you want to use n8n **Import from URL**.
3. Open `docs/N8N-IMPORT-URLS.md`.
4. Replace `YOUR_GITHUB_USERNAME` if required.
5. Import each raw JSON URL into n8n.
6. Connect Telegram, Google Calendar and OpenAI credentials.
7. Test before activating workflows.

## Phase 1

Current workflows provide:

- Telegram-based Concierge Orchestrator
- Google Calendar context
- Daily brief at 08:00 Asia/Dubai
- Weekly plan every Sunday at 17:00 Asia/Dubai
- Opportunity scoring from 0 to 100

## Important

Phase 1 does not yet include live scraping or authenticated access to InterNations, Privilee, Meetup or Eventbrite.

The workflows are designed not to invent live events when no discovery data is connected.
