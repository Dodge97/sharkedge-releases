# BetMGM Bot — Installation Guide

## What you need

- A Windows PC (Windows 10 or later)
- A BetMGM.nl account (email + password)
- A Relay API key (you'll receive this separately)

## Installation

1. Go to the [Releases page](https://github.com/Dodge97/betmgm-bot-releases/releases/latest)
2. Download **`BetMGM-Bot-Setup.exe`**
3. Double-click the installer → Next → Install → Finish
4. The app starts automatically — a green **B** icon appears in your system tray (bottom-right of your taskbar)
5. Your browser opens the setup wizard at `http://127.0.0.1:8095`

## Setup wizard

The wizard walks you through 4 steps:

1. **PIN** — choose a 4-6 digit code to protect your dashboard
2. **BetMGM credentials** — your BetMGM.nl email and password
3. **Relay API key** — paste the key you received
4. **Stake** — your default bet amount (e.g. €1.00)

After completing the wizard, the bot starts running in the background.

## Using the bot

- The green **B** icon in your system tray shows the bot is running
- **Right-click** the icon → Dashboard to open the web interface
- The dashboard shows your bets, P&L, win rate, and charts
- Use **Settings** to change your stake or switch between dry-run and live mode

> **Note:** The bot starts in **dry-run mode** by default — it logs bets without actually placing them. Switch to **live mode** in Settings when you're ready.

## Updates

When a new version is available, a yellow banner appears at the top of your dashboard:

1. Click **Download** — the installer downloads to your Downloads folder
2. Close the bot (right-click tray icon → Quit)
3. Run the new installer — your settings and data are preserved

## Troubleshooting

| Problem | Solution |
|---------|----------|
| No tray icon visible | Click the **^** arrow in your taskbar to find hidden icons |
| Browser doesn't open | Go to `http://127.0.0.1:8095` manually |
| "Connection refused" | Make sure the bot is running (check tray icon) |
| Forgot your PIN | Delete `%APPDATA%\BetMGM-Bot\bets.db` and restart (this resets all data) |

## Uninstalling

Use **Add/Remove Programs** in Windows Settings. Your betting data in `%APPDATA%\BetMGM-Bot` is preserved — delete that folder manually if you want a clean removal.
