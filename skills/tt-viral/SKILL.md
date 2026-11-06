---
name: tt-viral
description: >-
  Find what is actually working in the user's niche on TikTok and rank it by
  how far each video beat its own creator, then name the formula. Use for
  "what's working right now", "find viral videos in my niche", "why did this
  blow up", competitor research, or a swipe file.
---

# tt-viral

Raw view counts rank creator size, not ideas. This ranks by **multiple over each creator's own
median**, which is the only version of the question that is about the video.

```bash
python3 swipe.py collected.json --min 2.0
```

## Collecting the input

You need at least **four videos per creator** or a median means nothing, and the tool will skip
the creator and tell you it did. Collect them however the user prefers: the user reads the numbers
off their own phone screen and pastes them (they are already logged in), a public analytics site,
or a web search for public posts and accounts.

**Read, do not scrape.** Public listings only, never a logged-in session, never the user's own
account credentials, never a password. TikTok has no public API path in this pack on purpose.

Paste format (one video per line, `|` separated), then normalize into the JSON the tool reads:

```
@creator | 1.2M | first line of the hook or caption | url | 0:41
```

```json
[{"creator":"...","title":"...","views":412000,"url":"...","duration":41}]
```

## Reading the output

The multiple is the signal. A 400K video on a creator whose median is 30K outranks a 2M video on a
creator whose median is 2M. 3x and above is a strong signal; under 1.5x is that creator's normal
day. Say the sample size out loud: 12 videos is an anecdote, 40 across 6 creators is evidence.

The formula line is a judgement about the HOOK, matched against
[the 18 formulas](../tt-script/hooks.json) - it is not a claim about why the video worked, and you
should say so when you present it.

What to hand back: the top five with their multiples, the formula each used, and the ONE structural
thing they share. Then the harder line - which of those the user could actually make this week, in
their voice, with what they have. For a faceless teardown channel, prefer winners whose format is
animation, demonstration or mechanism-led, not talking head.

Save the winners to `~/.claude/tiktok/swipe.md` so `/tt-script` can read them next run: creator,
multiple, hook formula, and the one structural thing, nothing more.

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
