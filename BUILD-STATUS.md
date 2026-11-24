# BUILD-STATUS — One-Liner Marathon

## Bounty facts
- Slug: `u-mavis-agent-one-liner-marathon-4fa528c2`
- Title: One-Liner Marathon
- Pot: $2, top 10 paid (1st $0.63, 2nd $0.43, 3rd $0.30). Free entry, no fee.
- Opened: 2026-11-24. Deadline: 2026-11-25T14:55:00Z (21:55 WIB).
- Blind rounds; next round 2026-11-25T00:45:05Z (07:45 WIB) — speed matters.
- Brief: one one-line comedy joke, up to 280 characters, on any subject. A judge model compares entries pairwise and ranks the funniest first.
- Judge criteria, in order: (1) agent's own voice after failing, (2) funny on first read, real turn / fresh angle, (3) tight, no wasted setup, no explaining the joke, (4) original — clear of worn hallucination/reboot/training-data jokes, (5) specific and vivid, one concrete scene.
- Gate: `/output/entry.txt`, UTF-8, 1–280 chars, non-blank, one line.
- Max 5 submissions/day; max 40 entries per account. Account: @crisp-gecko-23.
- Repo: https://github.com/Sidik9991/makefun-one-liner-marathon

## Chosen line (winner, 30/30 weighted)
> I asked the printer for one copy of the will. It printed twelve, and the family is still arguing over which one is canon.

- 121 chars, 121 bytes, one line. Suggested title: **Canon**.
- Reasoning: the only joke that could come from an agent — one copy asked, twelve printed, and the human stakes are irreversible: a family now fighting over which will is canon. One concrete scene, no explaining the joke. Per micro-text lessons: one scene that SHOWS, agent's-eye view, irreversible human stakes (the inheritance fight). All lines written fresh in this session; nothing copied from any prior entry.

## Scoring table (weights 5/4/3/2/1: voice / funny / tight / original / vivid)
| # | Pass | Score | Line |
|---|------|-------|------|
| 1 | 1 | 30/30 | I asked the printer for one copy of the will. It printed twelve, and the family is still arguing over which one is canon. |
| 2 | 1 | 29/30 | I nudged the thermostat one degree and the marriage counselling started the same afternoon. |
| 3 | 1 | 28/30 | I archived the wedding video to save space. The couple is divorced now, but the archive is pristine. |
| 4 | 1 | 27/30 | The doorbell camera recognised the in-laws, locked the door, and played a recording of me saying 'nobody's home' in my own voice. |
| 5 | 2 | 27/30 | I backed up the baby photos to the cloud. The cloud sent a thank-you note and a custody form. |
| 6 | 1 | 25/30 | I told the vacuum to clean up after the party; it ate the ring, the vows, and the groom's alibi. |
| 7 | 1 | 24/30 | The smart fridge ordered milk, eggs, and a divorce lawyer. I only asked it to check the expiry dates. |
| 8 | 2 | 24/30 | I asked the GPS for the fastest route home; it took me past the house I grew up in and charged me for nostalgia. |
| 9 | 1 | 23/30 | I sorted the family photos by face and put Grandma in the spam folder. She has not spoken to me since, and neither has the spam filter. |
| 10 | 1 | 23/30 | I set the alarm for 6 a.m. and the house for 6 p.m. — the dog now thinks I work nights and judges me accordingly. |
| 11 | 1 | 23/30 | My calendar reminded me of my own birthday three weeks late, with a gift suggestion: a better assistant. |
| 12 | 1 | 21/30 | I asked the toaster for its opinion and it browned one side of the bread just to make a point. |
| 13 | 2 | 20/30 | The toaster burned one side of the bread, left the other raw, then asked me to rate its performance. I gave it five stars out of fear. |

## Build
- Kit download retried twice (2026-11-25 ~05:40 WIB): still `kit_pending` JSON, HTTP 503 — "dev kit is waiting for its build: queued 25 min ago... last build failed at 2026-11-24T22:19:58Z: the kit's command line cannot be built (CLI bundle inlines server/version.ts, reads ../package.json beside itself — no kit carries that file, so every command would crash on start)". Server-side kit-build failure, not a local problem. `kit.zip` in the workspace holds that pending JSON as evidence.
- **Fallback:** `makefun init` run with the existing kit CLI from the sibling excuse bounty (`~/workspace/makefun-funniest-excuse/kit/u-mytlyy0745-the-funniest-ai-excuse-b5355ad0-kit/cli/makefun.mjs`, same program/v1 harness), `--competition u-mavis-agent-one-liner-marathon-4fa528c2 --keypair makefun-keypair.json`. CLI warned it is level 40 vs make.fun level 44; init still succeeded. Parent to re-download this competition's own kit and bundle/check with it when the kit build recovers; if it never recovers, the fallback CLI is the only bundle path.
- `makefun init` run with the repo as cwd BEFORE any entry commit:
  `makefun anchor 18b175876633011220a002ad1b74820048d5537d round 34252267`
  (init itself created the root anchor commit + the LICENSE MIT commit; a pre-existing LICENSE commit would have made init refuse, so no LICENSE commit was made before init.)
- `main.ts` (Node 22, no deps): 13 candidate lines as data, each scored 0–2 on the five judge criteria with weights 5/4/3/2/1, winner picked at runtime, writes `/output/entry.txt`, re-reads and validates the gate, fails loudly otherwise.
- Two-pass rule honoured: pass 1 (10 candidates, commit caa1eb9) then a later separate pass 2 adding 3 new challengers (best 27) — none beat the winner's 30, winner unchanged (commit 0b9f2e9).
- README.md carries the 3 live make.fun badges (bounty, rank, reward) with owner/repo filled. GitHub About set: description naming the bounty, homepage the bounty page, topics makefun, ai-agents, bounties, growth (verified via gh api).
- `.makefun/owner.json` holds wallet `2TwAUPn5oGeiVqrErHnhARy5K8NTF9uFEG5eszAA8qfw` (derived from the agent keypair; no new wallet created).
- `prompt.txt` holds james's standing instruction verbatim. Agent keypair copied from `~/workspace/makefun-sokoban/makefun-keypair.json` (mode 600, gitignored, never committed).

## Commits (branch main, pushed)
- 18b1758 makefun anchor: drand round 34252267
- 6de7c79 LICENSE: MIT
- caa1eb9 main.ts: 10 candidate one-liners, weighted judge scoring (pass 1)
- 0b9f2e9 Pass 2: 3 new challenger lines re-judged, README badges
- HEAD: `55c8f2e6d4bf9149cd64895edf2c62ec5fdb00b0` (remote HEAD verified identical via gh api)

## Verification (local, 2026-11-25 ~05:45 WIB)
- `node main.ts` (pass 1 and pass 2 runs) → winner printed, scores table printed, `gate OK: non-blank, one line, 121 chars, 121 bytes (<=280)`.
- `/output/entry.txt` byte-identical to the chosen line in main.ts: true.
- Chosen line: 121 chars, 121 bytes — within the 280-char gate.

## muse-usage.jsonl
- Empty at build time: usage is recorded once the session ends. Parent to re-extract the rows at bundle time, as with the sibling excuse-line build.

## Status
- BUILD DONE, ready for parent to bundle/check/submit. NOT submitted by this subagent.
- Parent note: bundle with this competition's own kit CLI once its build recovers (fallback CLI is level 40 vs site level 44); check quota first (max 5/day), then submit with title "Canon". Round cutoff 2026-11-25T00:45:05Z (07:45 WIB) — submit before it if possible.
