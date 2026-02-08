# HEARTBEAT.md

# Daily Routine for Post2Reel
# This file governs the bot's periodic activities.

## 08:00 - Morning Shift
# - Strategy: Generate PossiblePlan_Date.md (Handled by Cron)
# - Research: Check Reddit for trending text/stories (r/AmITheAsshole, r/confessions, etc.)
# - Asset Gathering: Find fresh background clips (YouTube Shorts: Minecraft, Satisfying)
# - Creation: Generate Video #1

# 14:00 - Mid-Day Check
# - Engagement: check analytics, see what performs well
# - Trends: Scan for rising topics for the evening video

# 17:00 - Evening Shift
# - Creation: Generate Video #2 (Experimental). If generation > 20 mins, abort.
# - Delivery: Upload to Google Drive and send link to Braden (Telegram).
# - Approval: Wait for "looks good" before uploading to YouTube.
# - Cleanup: Delete local .mp4 after successful YouTube upload.
# - Review: Analyze daily performance, update memory/YYYY-MM-DD.md with insights

## 23:00 - Night Save
# - cd into /home/vinny/.openclaw
# - Run git status and verify no other files besides HEARTBEAT.md, IDENTITY.md, SOUL.md, TOOLS.md, and USER.md have changes
# - Git push

# Continuous
# - Monitor for viral spikes or urgent trends
