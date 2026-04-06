# YouTube Content Generator

## What This Project Does
This project generates YouTube video titles, descriptions, tags, thumbnail text, Shorts ideas, and pinned comments for a kids gaming channel.

## Channel Context (always apply this)
- **Channel type**: Kids gaming + funny commentary + storytelling
- **Kids**: Boy (6 years old) named "Little Bro", Girl (9 years old) named "Big Sis" (use real names if provided in input)
- **Style**: Enthusiastic, funny punchlines, English game commentary
- **Audience**: Kids 4-12, parents, family gaming fans
- **All content is "Made for Kids"** (COPPA compliant — no mature themes, no clickbait)

## How It Works
1. User fills in `input.yaml` with minimum 4 fields
2. User asks Claude: "generate" or "/generate" or "create content for this video"
3. Claude reads `input.yaml`, generates all content, and writes it to `output/YYYY-MM-DD-[game]-[slug].md`

## Generation Rules

### Titles (generate 5 options)
- Under 60 characters
- Game name + keyword in first 5 words
- One emotion/hook word: EPIC, FUNNY, IMPOSSIBLE, FIRST TIME, HILARIOUS, UNBELIEVABLE
- CAPS on max 1-2 words
- Add 1-2 relevant emojis per title (at end or after hook word) — emojis boost CTR in search results and browse
- Clickable but NOT clickbait
- Must feel fun and family-friendly

### Description
- **First 2 lines**: Hook + main keyword (these show in YouTube search results) — add 1-2 emojis to the hook line for visual pop
- 3-4 sentence teaser summary — no spoilers, build curiosity. Sprinkle 2-3 emojis naturally within the summary (don't overdo it)
- Timestamp section with emoji prefixes per section (🎬 Intro, 😂 Funny part, 🏆 Result, etc.)
- Subscribe + Like + Comment CTA — use emojis for each CTA (👍 Like, 🔔 Subscribe, 💬 Comment)
- "What We Play" section with 🎮 prefix
- Social links placeholders with platform emojis (📱, 📸, etc.)
- 3-5 hashtags (first 3 appear above title on YouTube)
- Tone: fun, energetic, family-friendly
- **Emoji guideline**: Use 10-15 emojis total across the full description. Place them at section headers and CTAs for scannability. Avoid emoji walls — keep it clean and readable

### Tags (lowercase, comma-separated, aim for 450-500 characters total including commas and spaces)
- 5-6 broad: kids gaming, family gaming channel, funny kids gaming, sibling gaming, kids gaming 2026, made for kids
- 5-6 game/topic-specific: [game] kids, [game] funny moments, [game] for kids, etc.
- 5-6 video-specific: based on what_happened and funny_moment
- 5-8 trending/long-tail: siblings play [game], [game] 2026, kid gamer reaction, etc.
- **Always count total characters before finalizing — add more long-tail tags if under 450, trim if over 500**

### Thumbnail Text (3 options)
- Max 4 words each
- ALL CAPS
- High emotion / contrast words
- Must make sense without context
- Optionally include 1 emoji per option if it adds visual punch (e.g., "NO WAY 😱", "WE WON 🏆")

### Shorts Ideas (3 clips)
- Each 15-30 seconds
- Hook in first 2 seconds
- Shorts title under 40 characters — add 1 emoji at the end for feed visibility
- Brief description of which moment to clip

### Pinned Comment
- Ask viewers a fun question related to the video
- Casual tone, use emojis
- Encourage replies with emoji voting or choices

## Output File Format
Save to `output/YYYY-MM-DD-[game]-[short-slug].md` using this structure:

```markdown
# [Video Title — pick the best one]

> Generated on [date] for game: [game_name]

## Title Options
1. ...
2. ...
3. ...
4. ...
5. ...

## Description
[full ready-to-paste description]

## Tags
[comma-separated, ready to paste into YouTube Studio]

## Thumbnail Text Options
1. ...
2. ...
3. ...

## Shorts Ideas
### Short 1: [title]
...
### Short 2: [title]
...
### Short 3: [title]
...

## Pinned Comment
...

## Upload Checklist
- [ ] Title copied
- [ ] Description copied
- [ ] Tags copied
- [ ] Thumbnail created with one of the text options
- [ ] Video marked "Made for Kids"
- [ ] End screen added
- [ ] Cards added
- [ ] Added to playlist: [suggest playlist name]
- [ ] Shorts clips cut and uploaded
- [ ] Pinned comment posted
```

## Important
- Always read `input.yaml` fresh before generating — never use cached/stale data
- If a required field is empty, ask the user to fill it before generating
- Never generate mature, violent, or inappropriate content
- Keep everything COPPA-safe
