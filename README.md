# Shipdeck (alpha)

Shipdeck is a native macOS app for people who ship several apps, games and websites on their own. It puts
every product in one place: what changed since the last release, what needs a release, and what the App
Store says. Claude Code reads each repo to fill in the details, and you review everything before it is saved.

Website: [shipdeck.taiphanvan.dev](https://shipdeck.taiphanvan.dev)

## Download

**[Download Shipdeck.zip](https://github.com/phanvantai/Shipdeck-releases/releases/latest/download/Shipdeck.zip)**,
unzip it and move `Shipdeck.app` to Applications. The app is signed and notarized by Apple.

## What you need

- macOS 15 or later.
- [Claude Code](https://claude.ai/code), installed and signed in (`claude` in Terminal). Shipdeck uses it to
  read your repos and runs it in its sessions. It works with Claude Code only for now: other coding agents
  (Codex, Gemini CLI, Cursor) aren't supported yet.
- Apple's Command Line Tools for git. Most developers have them through Xcode; if not, Shipdeck offers to
  install them.
- Optional: an App Store Connect API key, to see versions, TestFlight and reviews of your iOS apps.

Shipdeck is free during the alpha.

## Privacy

- Your portfolio is stored on your Mac, in `~/Library/Application Support/Shipdeck`. Shipdeck has no server
  and collects no analytics.
- When Shipdeck surveys a repo, Claude Code reads its files and sends them to Anthropic through your own
  Claude account, as any Claude Code session does. Files ignored by git and common secret files (`.env`,
  signing keys) are blocked from the survey.
- App Store Connect keys stay in your login keychain and are only sent to Apple.

## Feedback

Something broke, or something is missing? [Open an issue](https://github.com/phanvantai/Shipdeck-releases/issues/new?template=feedback.yml),
or choose **Help › Send Feedback…** in the app, which fills in your version and macOS.

## Updates

Shipdeck checks `appcast.xml` in this repo once a day and offers new versions in the app. Each update is
signed, and Shipdeck verifies the signature before installing.

The source code is private. This repo holds the release builds, the update feed and the issue tracker.
