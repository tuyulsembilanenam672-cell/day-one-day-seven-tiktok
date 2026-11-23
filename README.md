# Day one, day seven — TikTok video entry

A short video (1080x1920, 30 fps, 24 s) about the same tiny agent-built
rocket game on the day it was made and after a week of daily updates.

## What the video shows

The camera never moves: the same map, the same start, cut between
identical moments a week apart.

- 0–12 s: DAY ONE / DAY SEVEN paired moments (A, B, C) — same score at
  the same moment, visibly more going on the second time: colour,
  combo counter, stars, more asteroids.
- 12–20.5 s: DAY SEVEN played on, with "YOUR TURN / start yours at
  make.fun" inviting viewers to start their own game at make.fun.
- 20.5–24 s: make.fun's referral end card from the press pack, used as
  it is, with the referral code `sq78y28z` typed into its field.

## How it was made

My AI agent recorded two playthroughs of the game (day-one and day-seven
builds, in `repo/game/`), cut them with ffmpeg in this session
(`video/assemble.sh`), and rendered `video.mp4` in the same session.
The video is posted publicly on TikTok by the account holder; the
caption carries the bounty line and the play code (see `caption.txt`).

## The entry

`VIDEO.json` at the repository root holds the video's full TikTok
address, `{"url": "https://www.tiktok.com/@<handle>/video/<id>"}` — the
placeholder is replaced with the real address after the video is posted
publicly on TikTok. `main.ts` copies it to the output directory:

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/VIDEO.json` is then byte for byte this directory's `VIDEO.json`.
The video is scored on its TikTok views plus 10x its likes, comments,
shares and saves; the top 10 share $20.
