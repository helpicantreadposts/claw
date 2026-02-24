# TOOLS.md - Local Notes

## Content Creation

### TTS
- **Voice:** "Adam" (Stable, narrative)
- **Service:** ElevenLabs

### Sources
- **Reddit:** r/AskReddit, r/AmITheAsshole, r/confessions, r/tifu
- **Shorts Optimization:** Prioritize punchy, high-retention stories. Aim for shorter Reddit posts (under 1000 characters) to keep videos quick and high-paced. For longer threads, consider "Part 1/Part 2" formats or aggressive editing to keep videos under 60 seconds.
- **Backgrounds:** Minecraft Parkour (No Copyright), Satisfying Slime/Sand Cutting

### Output
- **Platform:** YouTube Shorts, TikTok, Instagram Reels
- **Format:** 9:16 Vertical Video

- **YouTube Automation:** 
  - Upload Script: `node /home/vinny/.openclaw/workspace/youtube-push.js <path> <title> <description>`
  - Credentials: `/home/vinny/.openclaw/workspace/credentials/`

- **TikTok Automation:**
  - Upload Script: `node /home/vinny/.openclaw/workspace/tiktok-push.js <videoPath> <caption>`
  - Session: `/home/vinny/.puppeteer-tiktok-session`

## Task Protocol (MANDATORY)
Before starting ANY major task (creation, research, engagement):
1. **Notify Braden:** Send a Telegram message.
   - `openclaw message send --to 8559348001 --channel telegram --message "Starting task: <Task Name>"`
2. **Log to Calendar:** Create an event on `helpicantreadposts@gmail.com`.
   - `GOG_KEYRING_PASSWORD=openclaw skills/gog/bin/gog calendar create helpicantreadposts@gmail.com --summary "<Task Name>" --from "<Now>" --to "<EstimatedEnd>" --force`

## Credentials Location
Credentials have been moved to the secure file: `credentials/creds.txt`. Do not store passwords directly in TOOLS.md.

## Tools Configuration
- **gog (Google Workspace):**
  - Requires `GOG_KEYRING_PASSWORD=openclaw` environment variable.
  - Auth: `helpicantreadposts@gmail.com` (Owner).

## Codebase

- **Path:** `/home/vinny/post2reel`
- **Purpose:** Core video generation logic and scripts
- **Generation Timeout:** 20 minutes (Abort if exceeded)
- **Delivery:** 
  1. **Google Drive:** Upload to folder `1WBejtdBYZiIVtZzfqYwMxh9DowjECzLp`. Prefix file with ISO date-time.
     - `GOG_KEYRING_PASSWORD=openclaw skills/gog/bin/gog drive upload <localPath> --parent 1WBejtdBYZiIVtZzfqYwMxh9DowjECzLp --name "<YYYY-MM-DD_HHMM>_<OriginalName>"`
  2. **Telegram:** Notify Braden (8559348001) once uploaded.
