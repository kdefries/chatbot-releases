# Illumibotto

An AI chat bot for your Twitch channel, packaged as a Windows desktop app. It joins your chat under a Twitch account **you** choose, replies when chatters mention it (powered by Google Gemini), can answer factual questions with live web search, and comes with configurable personalities.

This repo hosts the installers. Download the latest from the [Releases page](../../releases/latest).

## Install

1. Download `Illumibotto-Setup-<version>.exe` from the latest release.
2. (Optional) Verify the download against `SHA256SUMS` from the same release.
3. Run the installer. If Windows SmartScreen appears, choose **More info → Run anyway** (the installer is not code-signed).

The app updates itself from this repo - no GitHub account needed.

## First-run setup

The setup wizard walks you through everything:

1. **Connect the bot's Twitch account.** Sign in with the account the bot should chat as - a dedicated bot account is recommended (create one at twitch.tv like any normal account). **That account's name becomes your bot's name**: it's what chatters @mention to talk to it. You'll enter a short code at `twitch.tv/activate`; no passwords ever touch the app.
2. **Add an AI key.** Paste a free Google Gemini API key (get one at [aistudio.google.com](https://aistudio.google.com/apikey)). Optionally add a free [Tavily](https://tavily.com) key so the bot can answer factual questions with live web search.
3. **Pick your channel.** Enter the Twitch channel the bot should join and choose a starting personality.
4. **Mod the bot.** Type `/mod <botname>` in your channel's chat so the bot can reply without rate limits.

## Everyday use

- **Dashboard** - start/stop the bot and see its status. The bot replies while your stream is live.
- **Talking to the bot** - chatters @mention the bot's name (or just name-drop it), or use `!ask <question>` for a web-grounded answer. Mods can switch personalities with `!personality <name>`.
- **Bot config** - everything about the bot itself:
  - **Account**: see which Twitch account the bot runs as, or switch to a different one. Advanced users can supply their own Twitch application client ID.
  - **Aliases**: extra names the bot answers to (e.g. a nickname chat already uses).
  - **Personalities**: edit how the bot talks, or create new personalities.
  - **Test chat**: try the bot offline - the real reply pipeline with no Twitch connection.
- **Channels** - per-channel behavior: cooldowns, daily budgets, safety filter, commands.
- **Settings** - app options and updates.

## Requirements

- Windows 10/11
- A Twitch account for the bot (a dedicated one is recommended)
- A free Google Gemini API key
