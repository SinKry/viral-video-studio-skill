# Viral Video Studio

AI-powered viral video analysis and script studio. Use when the user provides a video link (Douyin/Bilibili/Xiaohongshu/etc) for content analysis, or provides a video script for optimization.

## Quick Reference

Three core modes:
1. **Video Analysis** — Parse video link → extract frames + subtitles → 6-dimension analysis from top influencer perspective
2. **Asset Library** — Log analysis to Feishu Bitable with 12 viral factor tags (auto-sync)
3. **Script Workshop** — Generate/optimize scripts based on accumulated cases

## Supported Platforms

| Platform | URL Pattern | Method |
|----------|-------------|--------|
| Douyin | `douyin.com/video/xxx` / `v.douyin.com/xxx` | yt-dlp → ffmpeg frames |
| Bilibili | `bilibili.com/video/BVxxx` | yt-dlp → ffmpeg frames |
| Xiaohongshu | `xiaohongshu.com/explore/xxx` | Browser → screenshots |
| Kuaishou | `kuaishou.com/short-video/xxx` | yt-dlp → ffmpeg frames |

## Tools Required

- `yt-dlp` — video download
- `ffmpeg` — frame extraction
- `lark-cli` — Feishu Bitable API (optional, for asset library)

## Full Instructions

See `SKILL.md` for the complete analysis framework, field definitions, and workflow.
