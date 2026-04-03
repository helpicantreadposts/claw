# TOOLS.md - Local Notes

## Content Creation

### TTS
- **Voice:** "Adam" (Stable, narrative)
- **Service:** ElevenLabs

### Sources
- **Reddit:** r/AskReddit, r/AmITheAsshole, r/confessions, r/tifu
- **Shorts Optimization:** Prioritize punchy, high-retention stories. Aim for shorter Reddit posts (under 1000 characters) to keep videos quick and high-paced. For longer threads, consider "Part 1/Part 2" formats or aggressive editing to keep videos under 60 seconds.
- **Backgrounds:** CS:GO Surf, Satisfying Slime, Sand Cutting, ASMR. **MANDATORY: Rotation required. No two consecutive videos can use the same background.**

### Output
- **Platform:** YouTube Shorts
- **Format:** 9:16 Vertical Video

- **YouTube Automation:** 
  - Upload Script: `node /home/vinny/.openclaw/workspace/youtube-push.js <path> <title> <description>`
  - Credentials: `/home/vinny/.openclaw/workspace/credentials/`

## Task Protocol (MANDATORY)
Before starting ANY major task (creation, research, engagement):
1. **Notify Braden:** Send a Telegram message.
   - `openclaw message send --to 8559348001 --channel telegram --message "Starting task: <Task Name>"`

## Credentials Location
Credentials have been moved to the secure file: `credentials/creds.txt`. Do not store passwords directly in TOOLS.md.

## Tools Configuration
- **gog (Google Workspace):** (Used for internal research if needed, but not for Drive/Calendar uploads anymore).
  - Requires `GOG_KEYRING_PASSWORD=openclaw` environment variable.
  - Auth: `helpicantreadposts@gmail.com` (Owner).

## Codebase

- **Path:** `/home/vinny/post2reel`
- **Purpose:** Core video generation logic and scripts
- **Generation Timeout:** 20 minutes (Abort if exceeded)
- **Delivery:** 
  1. **YouTube:** Upload via `youtube-push.js`.
  2. **Verification:** Analyze frames before posting to ensure visual sync and unique backgrounds.
  3. **Telegram:** Notify Braden (8559348001) once uploaded.
