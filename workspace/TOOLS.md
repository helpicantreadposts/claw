# TOOLS.md - Local Notes

## Content Creation

### TTS
- **Voice:** "Adam" (Stable, narrative)
- **Service:** ElevenLabs

### Sources
- **Reddit:** r/AskReddit, r/AmITheAsshole, r/confessions, r/tifu
- **Backgrounds:** Minecraft Parkour (No Copyright), Satisfying Slime/Sand Cutting

### Output
- **Platform:** YouTube Shorts, TikTok, Instagram Reels
- **Format:** 9:16 Vertical Video

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