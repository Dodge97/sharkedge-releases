# SharkEdge — Getting Started

SharkEdge is an automated sports betting agent. It monitors sharp betting markets, detects when your bookmaker's odds are too high, and places bets for you — fully automated, 24/7.

## What you need

- A **Windows** PC (Windows 10 or later) or a **Mac** (macOS 12 or later)
- An account at one or more supported bookmakers:
  - **BetMGM.nl**
  - **Toto.nl**
  - **BetCity.nl**

---

## Download & Install

### Windows

1. Go to the [latest release](https://github.com/Dodge97/sharkedge-releases/releases/latest)
2. Download **`SharkEdge-Setup.exe`**
3. Double-click the installer and follow the steps
4. SharkEdge starts automatically — a small icon appears in your **system tray** (bottom-right, near the clock)

> **Windows SmartScreen warning?** Click **More info** → **Run anyway**. This appears because the app is new — it is safe to proceed.

### macOS

1. Go to the [latest release](https://github.com/Dodge97/sharkedge-releases/releases/latest)
2. Download the right DMG for your Mac:
   - **Apple Silicon** (M1/M2/M3/M4): `SharkEdge-...-Apple-Silicon.dmg`
   - **Intel** (2017–2020 models): `SharkEdge-...-Intel.dmg`
   - *Not sure?* Click **Apple menu → About This Mac**. "Chip: Apple M…" means Apple Silicon.
3. Open the DMG and drag SharkEdge into **Applications**
4. Open SharkEdge — if macOS shows a security warning, go to **System Settings → Privacy & Security → Open Anyway**

---

## Setup

When you first open SharkEdge, a setup wizard walks you through:

1. **Create your account** — enter your email address
2. **Accept the terms** — review and agree to the terms of service
3. **Choose a PIN** — protects your dashboard from others on your computer

After setup, go to **Settings** and connect at least one bookmaker account with your email and password. SharkEdge then starts placing bets automatically.

> **Keep your computer on** while SharkEdge is running. It needs to stay active to monitor markets and place bets. You can close the browser window — SharkEdge runs in the background via the system tray icon.

---

## Pricing

SharkEdge is **free to start**. Your first **€50 in profit is free of charge** — no fees at all.

After that, a **40% performance fee** applies only on **new profit**. You never pay fees on losses.

### How it works

The fee is based on a high-water mark — you only pay on profit that exceeds your previous peak. If your profit dips, the fee goes down too. You only pay again once you surpass your previous highest point.

**Example:**

| What happens | Your total profit | Fee (40% above €50 free) |
|---|---|---|
| You make €50 in profit | €50 | €0 — still within the free tier |
| You make another €30 | €80 | €12 — 40% on the €30 above the free €50 |
| You hit a losing streak, profit drops to €60 | €60 | €4 — fee drops automatically |
| You recover back to €80 | €80 | €12 — same as before, back to your peak |
| You push past to €100 | €100 | €20 — you only pay on the new €20 above your old peak |

### When do I pay?

When your accumulated fee reaches **€50**, a payment banner appears in your dashboard. You have **24 hours** to pay via the secure Stripe checkout. After payment, SharkEdge continues automatically. If not paid in time, SharkEdge pauses until the fee is settled.

Fees always reflect your current profit — if you're in a losing streak, the fee decreases and may drop below the €50 threshold, in which case the payment banner disappears.

---

## Updates

When a new version is available, a banner appears in your dashboard:

1. Click **Download**
2. Close SharkEdge (right-click the tray/menu bar icon → **Quit**)
3. Run the new installer — your settings and data are kept

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| **No tray icon visible** | **Windows:** Click the **^** arrow in your taskbar. **Mac:** Check the top-right menu bar. |
| **Dashboard doesn't open** | Go to `http://127.0.0.1:8095` manually |
| **"Connection refused"** | Make sure SharkEdge is running. If just installed, wait a few seconds and refresh. |
| **Won't start** | Try quitting and reopening the app |
| **Forgot your PIN** | On the login page, click **Forgot your PIN?** and enter the email you used during setup. Your PIN resets and all data is preserved. |
| **"Registration is currently closed"** | Contact the operator — new registrations may be temporarily paused. |
| **macOS: "not supported on this Mac"** | Make sure you downloaded the correct version (Apple Silicon or Intel). |

---

## Uninstalling

**Windows:** Settings → Apps → Installed Apps → SharkEdge → Uninstall

**macOS:** Drag the app from Applications to the Trash

Your betting data is preserved after uninstalling. To remove everything, also delete:

- **Windows:** `%APPDATA%\SharkEdge\`
- **macOS:** `~/Library/Application Support/SharkEdge/`
