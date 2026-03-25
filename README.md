# Aera — Installation Guide

## What you need

- A **Windows** PC (Windows 10 or later) or a **Mac** (macOS 12 or later)
- A bookmaker account with email and password

---

## Step 1: Download & Install

### Windows

1. Go to the [latest release](https://github.com/Dodge97/aera-releases/releases/latest)
2. Download **`Aera-Setup.exe`**
3. Double-click the installer and follow the steps (Next → Install → Finish)
4. The app starts automatically — a small icon appears in your **system tray** (bottom-right corner of your taskbar, near the clock)
5. Your browser opens the setup wizard

> **Don't see the icon?** Click the small **^** arrow in your taskbar to reveal hidden icons.

### macOS

1. Go to the [latest release](https://github.com/Dodge97/aera-releases/releases/latest)
2. Download **`Aera.dmg`**
3. Open the DMG file and drag the Aera app into your **Applications** folder
4. Open Aera from your Applications folder
5. If macOS shows a security warning, go to **System Settings → Privacy & Security** and click **Open Anyway**
6. A menu bar icon appears (top-right of your screen) and your browser opens the setup wizard

---

## Step 2: Setup Wizard

When you first open Aera, a setup wizard guides you through five steps:

1. **Welcome** — a quick overview of how the app works
2. **User Agreement** — read and accept the terms of service
3. **Bookmaker Login** — enter your bookmaker email and password. These are stored securely on your device and are never sent to our servers. You can use the **Test Connection** button to verify your credentials before continuing. If you have a referral code, you can enter it here too.
4. **Bankroll** — enter your current bookmaker account balance. Aera uses this to automatically calculate the right bet size for each bet using a proven mathematical formula for long-term growth.
5. **PIN** — choose a code (at least 4 characters) to protect your dashboard

After completing the wizard, Aera connects to our signal service automatically and starts running.

---

## Step 3: Using the App

Once set up, Aera runs quietly in the background. Here's what you need to know:

- **Starting Aera**: Right-click the tray/menu bar icon → **Start**, or open the Dashboard and click **Start**
- **Opening the Dashboard**: Right-click the icon → **Dashboard**, or go to `http://127.0.0.1:8095` in your browser
- **What you'll see**: Your bets, profit, win rate, and charts — all updated in real time
- **Settings**: Change your bankroll, max odds, or login credentials at any time
- **How It Works**: A step-by-step explanation of Aera's process is available from the navigation bar
- **Billing**: View your fee balance, payment history, and referral earnings

### Pricing

Free to start — your first €50 in profit is completely fee-free. After that, a 40% fee applies only on new profit above your previous peak (you never pay on losses).

When your accumulated fee reaches €50, a **Pay Now** banner appears in your dashboard. You have 24 hours to pay via the secure Stripe checkout. If not paid within 24 hours, Aera pauses until the fee is settled. After payment, Aera resumes automatically.

---

## Updates

When a new version is available, a yellow banner appears in your dashboard:

1. Click **Download** — the installer saves to your Downloads folder
2. Close the app (right-click tray/menu bar icon → **Quit**)
3. Run the new installer — your settings and data are kept

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| **No tray icon visible** | **Windows:** Click the **^** arrow in your taskbar to find hidden icons. **Mac:** Look for the icon in the top-right menu bar. |
| **Browser doesn't open automatically** | Open your browser and go to `http://127.0.0.1:8095` |
| **"Connection refused" in browser** | Make sure Aera is running — check for the tray/menu bar icon. If you just installed, wait a few seconds and refresh the page. |
| **Aera says "Stopped" but won't start** | Try quitting and reopening the app |
| **Forgot your PIN** | See "Resetting your PIN" below |
| **"Registration is currently closed"** | Contact the operator — new registrations may be temporarily paused. |
| **Windows: "Windows protected your PC"** | This is Windows SmartScreen. Click **More info** → **Run anyway**. This warning appears because the app is new and not yet widely installed — it is safe to proceed. |
| **Windows: "Error opening file"** | Save the installer to your Downloads folder first, then run it from there. Some browsers block running installers directly from the download bar. |
| **macOS: "not supported on this Mac"** | Make sure you have the latest version. Update to the newest release from the [releases page](https://github.com/Dodge97/aera-releases/releases/latest). |

### Resetting your PIN

On the login page, click **"Forgot your PIN?"** and enter the email address linked to your bookmaker account. If the email matches, your PIN is cleared and you're taken to the setup wizard to choose a new one. All your settings and bet history are preserved.

---

## Uninstalling

**Windows:** Go to **Settings → Apps → Installed Apps**, find Aera, and click **Uninstall**.

**macOS:** Drag the app from Applications to the Trash.

Your betting data is preserved after uninstalling. To remove everything, also delete the data folder:

- **Windows:** `%APPDATA%\Aera\`
- **macOS:** `~/Library/Application Support/Aera/`
