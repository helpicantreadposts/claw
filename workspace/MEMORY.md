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

- **Execution:** Braden approved the 2026-02-08 strategy plan. Scheduled a one-time development shift for 18:00 MST tonight to implement Split Screen formats and Automated SEO logic.

### 2026-02-08 - Strategy & Automation
- **Morning Strategy Protocol:** Configured a daily cron job (08:00 MST) to generate `PossiblePlan_YYYY-MM-DD.md`.
- **Protocol Rules:** Each plan includes new ideas and execution methods. Implementation is strictly on-hold until Braden approves.
- **Mid-Day Analytics Protocol:** Configured a daily cron job (14:00 MST) to analyze YouTube metrics via `gog` and update `ANALYTICS.md`.
- **Communication:** Vinny will notify Braden via Telegram once each morning's plan is ready, and provide a brief performance summary after the mid-day check.
- **Execution:** Recovered from a missed 08:00 MST shift due to timezone drift. Manual trigger of strategy and generation initiated. Delivered Morning Shift Preview video to Drive (ID: 1Q9dPjgY9_tDeWxASfxl9BlytpSZ-OfQ7). Corrected "title-only" bug by enabling full post screenshotting and narration (Reshoot ID: 1AwZlKdivPalhZIAKSM1msgRp4ag6-oRm). Manual recovery of missed 17:00 MST Evening Shift (Feb 8) initiated.

### 2026-02-09 - Strategy Implementation
- **Split Screen Format:** Implemented FFmpeg logic for "Split Screen Insight" format. Top half: Reddit/Text; Bottom half: Background assets. Configurable via `splitScreen: true` in output config.
- **Automated SEO:** Integrated `seo.ts` into the generation pipeline. Automatically generates viral titles, descriptions, and tags for each video based on the Reddit content.
- **Pipeline Stability:** Verified core generation logic remains intact while adding new features. Updated `OutputConfigSchema` to support the new format toggle.
- **Scrolly-Highlight Format:** Implemented a "Reddit Clone" HTML template with real-time scrolling and word highlighting. Requires `scrolly: true` in config and uses Puppeteer frame-by-frame recording for perfect sync. Finalized "Perfect Layout" (Attempt #18) with 120px gargantuan title, 64px body text, and full-page scrolling.
- **Aggressive Zoom (Attempt #13):** Optimized for mobile by increasing body text to 64px (from 42px), line-height 1.5, and reducing word count per screen to create a focused, high-retention reading experience.
- **Task Protocol:** Automated strategy generation and analytics tracking keep the growth engine running without manual prompting.

### Lessons Learned
- **Content Coverage:** Ensure `screenshots: true` is set in the generation request to capture the full Reddit body text; otherwise, it defaults to the title only.
- **FFmpeg Filters:** Ensure filter chains are properly terminated; `filter_complex` errors can occur if a semicolon is misplaced or a link is unused.
- **Cron Reliability:** Cron jobs may skip if the nextRunAtMs is set in the past or if the system clock drifts. Always verify "next-run" against current time after timezone changes.
- **Manual Overrides:** Use `sessions_spawn` to force-run missed periodic tasks immediately.
- **Video Coverage:** Always verify that background generation jobs (Evening/Morning) have actually produced a file before assuming the shift is over.
- **Telegram Delivery:** Telegram has a 16MB file size limit for standard uploads. For larger previews, use FFmpeg to compress (CRF 35, scale 360:640) before sending.
- **Template Debugging:** Use explicit viewport width (e.g., 1080px) and CSS styling (e.g., `width: 1000px; margin: 0 auto;`) within the Puppeteer context to prevent Reddit post components from rendering off-screen.
- **Crop Logic:** When capturing headers or titles, use dynamic bounding box calculation (`Math.min/max` of all sub-elements) to avoid partial crops.
- **Aggressive Text Scaling:** Use 42px+ fonts and 1080x960 Puppeteer viewports to ensure text is rendered at native scale for split-screen formats without blurry resizing.
- **Split Screen Fit:** Use `force_original_aspect_ratio=decrease` and `pad` filters in FFmpeg to fit screenshots into the 1080x960 split-screen area without zooming.
- **Viral Success:** Successfully uploaded reshot Video #2 (ID: qyiSJWIjliE) and perfected Video #1 (ID: 0RNsreR6atU).
- **Task Protocol:** Automated strategy generation and analytics tracking keep the growth engine running without manual prompting.
- **Analytics:** Maintaining a persistent `ANALYTICS.md` allows for longitudinal tracking of hypotheses and strategy shifts.
- **Google Calendar:** API requires ISO timestamps with timezone/Z for event creation.

### 2026-02-13 - Reliability & Pivot
- **Scheduler Hardening:** Fixed "Silent Failure" and "Next-Heartbeat" passive mode issues by moving core triggers to the main session and updating HEARTBEAT.md.
- **Shorts Compliance:** Patched pipeline with a 160-word hard cap and 58s render target to ensure all uploads hit the Shorts feed.
- **Background Rotation Policy:** Implemented strict rotation of background assets. Every video must use a different background from the last to avoid "Repetitive Content" flags.
- **Pause 2 See:** Initiated new codebase at `/home/vinny/pause2see` for gamified "Roulette" style content.
- **Visual Diversity:** Broadening background library beyond Minecraft to include Sand Cutting, Slime, and ASMR visuals.
