# mp3-extraction

An [Agent Skill](https://skills.sh) that teaches coding agents how to extract audio from video files with `ffmpeg` — MP3, M4A, WAV, FLAC, Opus, plus normalization and batch recipes.

```
npx skills add <your-github-user>/mp3-extraction
```

## What it does

When a user says *"extract the audio from this MP4"*, *"convert this video to MP3"*, or *"rip the sound out of this clip"*, the skill walks the agent through:

- Choosing **MP3 / M4A / WAV / FLAC / Opus** based on the goal
- VBR quality settings (`-q:a`) vs fixed bitrate
- Trimming, loudness normalization, light noise reduction
- Batch conversion and merging multiple files
- Verifying output with `ffprobe`

See [`SKILL.md`](./SKILL.md) for the full instructions.

## Quick example

```bash
ffmpeg -i input.mp4 -vn -codec:a libmp3lame -q:a 2 output.mp3
```

## Related

Prefer a browser tool instead of the command line? [MP4toMP3](https://mp4tomp3.to/) converts video to MP3 in the browser — free, no sign-up.

## Install

```bash
npx skills add <your-github-user>/mp3-extraction
```

Works with Claude Code, Codex CLI, Cursor, OpenCode, and [75+ other agents](https://github.com/vercel-labs/skills/blob/main/docs/agents.md).

## License

MIT
