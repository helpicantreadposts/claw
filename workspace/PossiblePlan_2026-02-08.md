# Platform Expansion and Technical Pipeline Improvements - 2026-02-08

## 1. Platform Expansion: X (Twitter)
### Concept
Automate the conversion of trending Reddit threads into "viral threads" on X using high-quality images and structured text.

### Execution Method
1. **Scraping:** Extract top comments from a target Reddit thread.
2. **Formatting:** Summarize each comment into < 280 characters using LLM.
3. **Visualization:** Use `canvas` tool or a local script to generate high-contrast images of the Reddit comments (to mimic the "screenshot" aesthetic that performs well).
4. **Posting:** Use a Python script with `tweepy` or a similar library to post the thread.
5. **Growth Strategy:** Tag the original subreddit or related niche accounts to drive engagement.

## 2. New Video Format: "Split Screen Insight"
### Concept
Instead of just gameplay background, use a split screen: Top half is the Reddit story text/visual, bottom half is a "Satisfying" video or a curated AI-generated landscape that matches the *mood* of the story.

### Execution Method
1. **Mood Analysis:** Use LLM to determine the "vibe" of the story (e.g., Scary, Heartwarming, Rage).
2. **Asset Retrieval:** Select from a local library of background categories based on mood.
3. **Assembly:** Update `post2reel` ffmpeg logic to support 1:1 or 2:1 vertical splits.

## 3. Technical Pipeline Improvement: Real-time Voice Cloning
### Concept
Move from standard TTS to cloned voices of popular "Storytime" creators (with permission/open-source models) or unique branded voices.

### Execution Method
1. **Implementation:** Integrate `Coqui TTS` or `OpenVoice` into the `back-end/src/generator/audio` module.
2. **Dynamic Inflection:** Use SSML or advanced LLM prompting to add "gasps," "pauses," and "emphasis" based on the text content to increase retention.

## 4. Technical Pipeline Improvement: Automated SEO & Metadata
### Concept
Automatically generate viral titles, descriptions, and tags for YouTube/TikTok/Instagram using historical performance data.

### Execution Method
1. **Data Tracking:** Log the performance (views/likes) of every generated video to a local `analytics.json`.
2. **Title Generation:** Prompt LLM with the story summary + "top performing title patterns" from the analytics file.
3. **Auto-Publish:** Update the `youtube-push.js` script to pull these generated fields automatically.
