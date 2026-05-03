# SharkEdge — Getting Started

**Bet where the market is going — before the odds move.**

SharkEdge finds profitable bets and places them for you — fully automated.

## How it works

1. **Scans the market** — monitors where sharp money is moving
2. **Places bets for you** — logs into your bookmaker and places the bet automatically
3. **Tracks everything** — results update live in your dashboard

Want to understand the math behind it? Check **How it works** in your dashboard after setup.

---

## What you need

- A **Windows** PC (Windows 10+) or **Mac** (macOS 12+)
- An account at one or more supported bookmakers:
  - **BetMGM.nl** · **Toto.nl** · **BetCity.nl** · **LeoVegas.nl** · **Bingoal.nl**

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

After setup, go to **Settings** and connect at least one bookmaker account — you'll need your bookmaker email/password and a starting bankroll (minimum €100). The bankroll tells SharkEdge how big each bet should be.

When the connection is saved, click the **play button next to the SharkEdge logo** in the sidebar to start. SharkEdge then places bets automatically.

---

## Keep it running

SharkEdge needs to stay active to monitor markets and place bets. Keep your computer on and don't quit the app. You can close the browser window — SharkEdge runs in the background via the system tray icon.

---

## Using SharkEdge on a VPS

If you run SharkEdge on a cloud VPS (Hetzner, OVH, ...), bookmakers may flag the account because the IP belongs to a datacenter range. Route bookmaker traffic through a Netherlands residential proxy:

1. Buy a static residential ISP proxy in the Netherlands (Decodo's "Static Residential" plan is recommended — about €2.50/month for one dedicated IP, unlimited bandwidth)
2. Open SharkEdge → **Settings → Connection**
3. Paste the proxy URL (looks like `http://user:pass@host:port`)
4. Click **Connect** — confirm the response shows "Netherlands"

That's it. All bookmaker traffic now routes through your NL proxy. SharkEdge will refuse to start if the proxy ever becomes unreachable; you'll get a modal pointing you back to **Settings → Connection** to fix or remove the proxy URL.

---

## Updates

When a new version is available, a banner appears in your dashboard:

1. Click **Download**
2. Close SharkEdge (right-click the tray/menu bar icon → **Quit**)
3. Run the new installer — your settings and data are kept

---

## Pricing

SharkEdge is **free to install and use**. Your first **€50 in profit is completely free**.

After that, a **40% performance fee** applies on new profit only — you never pay on losses. Full pricing details are in your dashboard under **Billing**.

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

## Running on a VPS (advanced)

Run SharkEdge 24/7 without keeping your own PC on. You'll need a Windows VPS and a Dutch residential proxy. Expect ~€8/month for the VPS and ~€25/month for the proxy.

**1. Buy an OVHcloud VPS** — plan **VPS-1** with Windows Server Desktop (4 vCore, 8GB RAM, 75GB NVMe), Europe region.

**2. Buy a Decodo proxy** — **Static Residential (ISP)**, location **Netherlands**, 3 IPs, unlimited traffic. Decodo gives you a host, port, username, and password.

**3. Log into the VPS** — on your own PC, open **Remote Desktop Connection**, enter the VPS IP from OVHcloud, and sign in with the OVH credentials. Then install SharkEdge inside the VPS using the Windows steps above.

**4. Set the proxy in SharkEdge** (inside the VPS, not your own PC):

1. Open **Settings → Connection** in SharkEdge
2. Paste the proxy URL as `http://USERNAME:PASSWORD@HOST:PORT`
   *Example:* `http://nl-user-1:s3cret@gate.decodo.com:7000`
3. Enter your SharkEdge PIN and click **Connect**

SharkEdge tests the proxy and shows the detected **IP**, **country**, and **ISP**. You should see a Dutch IP and a residential ISP — not OVH. If the test fails, double-check the URL and that the proxy is activated in your Decodo dashboard.

> Do **not** set a proxy in Windows Settings — SharkEdge ignores it.

---

## Uninstalling

**Windows:** Settings → Apps → Installed Apps → SharkEdge → Uninstall

**macOS:** Drag the app from Applications to the Trash

Your betting data is preserved after uninstalling. To remove everything, also delete:

- **Windows:** `%APPDATA%\SharkEdge\`
- **macOS:** `~/Library/Application Support/SharkEdge/`
