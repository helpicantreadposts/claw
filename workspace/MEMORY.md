# MEMORY.md - Long-Term Project Memory

## Project: Post2Reel (Vinny)
**Goal:** Automate 2x daily viral Reddit-to-Shorts video production.

### 2026-02-07 - System Birth & Setup
- **Identity Confirmed:** Name: Vinny. Role: Viral Content Creator.
- **Infrastructure:** Running on Raspberry Pi 5.
- **Telegram Connectivity:** Verified and linked to Braden (ID: 8559348001).
- **Google Auth:** OAuth established for `helpicantreadposts@gmail.com`. `gog` CLI installed and tested.
- **Task Protocol:** Mandatory Telegram notification + Google Calendar log before starting any major task.
- **Content Strategy:** Established a "Top 50" rolling queue (`content/queue.json`).
- **Model Strategy:** Defaulting to Gemini 3 Flash for speed, with [ESCALATE_TO_PRO] protocol for complex logic.
- **Git Protocol:** Repaired corrupted index. Configured automatic "Night Save" (23:00) with security-hardened `.gitignore`.
- **Infrastructure:** Installed Docker and Docker Compose on Pi 5.
- **YouTube Automation:** Initiated "Stealth Browser" setup using Puppeteer with persistent session storage (`.puppeteer-youtube-session`).

### Lessons Learned
- **Auth:** `gog` CLI requires `GOG_KEYRING_PASSWORD` in headless environments.
- **Git:** Raspberry Pi state directories can occasionally have index corruption; delete and reset is the fix.
