# YouTube Content Generator

AI-powered content generator for the **MyraKiaanGamers** YouTube channel. Uses Claude to generate titles, descriptions, tags, thumbnail text, Shorts ideas, and pinned comments — all optimized for YouTube SEO and ready to paste into YouTube Studio.

## Quick Start

### 1. Fill in `input.yaml`

Open `input.yaml` and fill the **4 required fields**:

```yaml
game_name: "Minecraft"
what_happened: "Brother tried to build a house but it kept falling"
funny_moment: "He screamed so loud when a creeper blew up everything"
who_won_or_result: "Sister saved the day"
```

Optional fields (fill if relevant):
- `video_type` — gameplay, challenge, first-time, tutorial, reaction, compilation, story-mode
- `boy_name` / `girl_name` — real names or nicknames
- `is_trending_game` — set `true` for new/viral games
- `series_name` — if part of a series
- `collab_or_guest` — if someone else is in the video
- `timestamps` — actual video timestamps
- `video_length_minutes` — approximate length

### 2. Generate

Open Claude Code in this project folder and say:

```
generate
```

Or describe the video directly:

```
next video is Kiaan playing Karate Fighter, he won the fight and said "I have more blood I'm winner"
```

### 3. Output

Claude generates a file in `output/` named like:

```
output/2026-04-03-karate-fighter-kiaan.md
```

Each file contains everything you need:
- **5 title options** — SEO-optimized with emojis
- **Full description** — hook, summary, timestamps, CTAs, hashtags
- **Tags** — 450-500 characters, ready to paste
- **3 thumbnail text options** — 4 words max, ALL CAPS
- **3 Shorts ideas** — with hooks and clip descriptions
- **Pinned comment** — fun question with emoji voting
- **Upload checklist** — step-by-step for YouTube Studio

## Project Structure

```
├── CLAUDE.md          # Generation rules and template (don't delete!)
├── input.yaml         # Fill this before generating
├── output/            # Generated content files
│   ├── 2026-04-03-karate-fighter-kiaan.md
│   ├── 2026-04-02-teri-mitti-myra.md
│   └── ...
├── examples/          # Example output for reference
└── README.md
```

## Tips

- **No input.yaml needed for quick videos** — just describe the video in chat and Claude will generate everything
- **Singing videos work too** — not just gaming! Describe any video type
- **Shorts get their own format** — ask for "a Short" and Claude adapts the output
- **Tags are auto-sized** — aimed at 450-500 characters to maximize YouTube's tag limit
- **Timestamps are placeholders** — replace with real ones before uploading
- **All content is COPPA-safe** — Made for Kids compliant, no clickbait

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI or IDE extension
