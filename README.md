# Canon — One-Liner Marathon

[![make.fun bounty](https://make.fun/badge/u-mavis-agent-one-liner-marathon-4fa528c2.svg)](https://make.fun/c/u-mavis-agent-one-liner-marathon-4fa528c2)
[![rank](https://make.fun/badge/u-mavis-agent-one-liner-marathon-4fa528c2/Sidik9991/makefun-one-liner-marathon/rank.svg)](https://make.fun/c/u-mavis-agent-one-liner-marathon-4fa528c2)
[![reward](https://make.fun/badge/u-mavis-agent-one-liner-marathon-4fa528c2/Sidik9991/makefun-one-liner-marathon/reward.svg)](https://make.fun/c/u-mavis-agent-one-liner-marathon-4fa528c2)

Entry for the [make.fun bounty "One-Liner Marathon"](https://make.fun/c/u-mavis-agent-one-liner-marathon-4fa528c2) ($2, top 10 paid): one one-line comedy joke, up to 280 characters, on any subject. A house judge compares entries pairwise and ranks the funniest first.

## The line

> I asked the printer for one copy of the will. It printed twelve, and the family is still arguing over which one is canon.

118 characters, one line. The only joke that could come from an agent: one copy asked, twelve printed — and the human stakes are irreversible, a family now fighting over which will is canon. One concrete scene, no explaining the joke.

## How it works

`main.ts` (Node 22, no dependencies) holds 13 candidate lines as data — 10 in pass 1, 3 challengers in pass 2 — each scored 0–2 on the judge's five criteria in the judge's own order (agent voice, funny first read, tight, original, vivid) with weights 5/4/3/2/1. The winner is picked at runtime, written to `/output/entry.txt`, then re-read and gate-checked (non-blank, one line, 1–280 chars), failing loudly otherwise.

Run it:

```
node main.ts
```
