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
- **Slack Integration:** Slack token added for `post2reel` notifications.
- **Visual Style:** Established preference for word-by-word text overlays following a Reddit post title screenshot.
- **Medium-Matching:** Implemented "Voice In = Voice Out" protocol for Telegram interactions using `faster-whisper` and `piper-tts`.

### 2026-02-08 - Strategy & Automation
- **Morning Strategy Protocol:** Configured a daily cron job (08:00 MST) to generate `PossiblePlan_YYYY-MM-DD.md`.
- **Protocol Rules:** Each plan includes new ideas and execution methods. Implementation is strictly on-hold until Braden approves.
- **Mid-Day Analytics Protocol:** Configured a daily cron job (14:00 MST) to analyze YouTube metrics via `gog` and update `ANALYTICS.md`.
- **Communication:** Vinny will notify Braden via Telegram once each morning's plan is ready, and provide a brief performance summary after the mid-day check.
- **Execution:** Successfully delivered a generated video to Drive and notified Braden via Telegram. Received approval and uploaded to YouTube (ID: XKqH0glmw_0). Local cleanup completed.

### Lessons Learned
- **YouTube Upload:** Standardized on `youtube-push.js` using Node.js/googleapis for API uploads.
- **Cron Jobs:** `cron.add` schedule requires `kind: "cron"` and `expr`.
- **Task Protocol:** Automated strategy generation and analytics tracking keep the growth engine running without manual prompting.
- **Analytics:** Maintaining a persistent `ANALYTICS.md` allows for longitudinal tracking of hypotheses and strategy shifts.
- **Google Calendar:** API requires ISO timestamps with timezone/Z for event creation.
