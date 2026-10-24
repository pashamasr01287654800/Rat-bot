# Configuration & Usage Guide

<p align="center">
  <img src="Rat-bot.png" alt="System Monitor Banner" width="700">
</p>

## 1. Telegram Bot Setup

### Create a Bot
1. Open Telegram and contact [@BotFather](https://t.me/BotFather).
2. Send `/newbot` and follow the instructions.
3. Store your Bot Token securely.

### Get Your Chat ID
1. Contact [@myidbot](https://t.me/myidbot) or [@userinfobot](https://t.me/userinfobot).
2. Start a conversation and copy your Chat ID.

> **Security:** Never publish real tokens or credentials in a public repository.

---

## 2. Configuration

Open the project's configuration file using your preferred text editor and enter your own credentials:

```ini
BOT_TOKEN=PASTE_YOUR_TOKEN_HERE
CHAT_ID=PASTE_YOUR_CHAT_ID_HERE
```

Keep configuration files containing real credentials out of public repositories.

---

## 3. Features & Capabilities

### Device Information
- `/info` — Display basic device information.
- `/online` — Check agent availability.
- `/battery` — Report battery status.

### Location Services
- `/location_gps` — Request a GPS location, subject to device permissions.
- `/location_net` — Request a network-based location, subject to device permissions.
- `/location_history` — View saved location history, if enabled.

Location accuracy and background operation depend on Android permissions, power-management settings, and device configuration.

### Other Commands
| Category | Commands |
|---|---|
| SMS | `/sms_dump`, `/sms_send` |
| Calls | `/call_log` |
| Contacts | `/contacts`, `/contacts_add`, `/contacts_del` |
| System | `/open_url` |
| App Controls | `/hide`, `/show`, `/status` |

Command availability depends on the build edition, implementation, and granted permissions. Use personal-data features only on devices you own or are explicitly authorized to administer, with informed consent.

---

## 4. Requirements

- Android device or emulator
- Telegram bot
- Required Android build tools for the selected build
- Apktool, where required by the project

Refer to the project's build script for edition-specific setup instructions.

---

## 5. Security & Privacy

- Use only on devices you own or are authorized to administer.
- Obtain informed consent before accessing personal data or location.
- Protect bot tokens and other private credentials.
- Review Android permissions and background-execution restrictions.
- Do not distribute builds containing real credentials.

---

## 6. Disclaimer

This project is intended for authorized device administration and legitimate security research. You are responsible for obtaining the necessary permissions and complying with applicable laws.

---

<p align="center">
  <sub>System Monitor Agent · Authorized Use Only</sub>
</p>








