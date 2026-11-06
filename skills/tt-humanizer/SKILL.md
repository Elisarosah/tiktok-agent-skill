---
name: tt-humanizer
description: >-
  Strip the AI fingerprint off a script or caption before it ships, so it
  sounds like the user wrote it. Use whenever the user wants a draft cleaned
  up, "make this sound like me", "remove the AI from this", or before anything
  goes out.
---

# tt-humanizer

A script that sounds written is a script nobody believes. The tells are small, and they are all
fixable by hand.

## Before you clean

1. Read `~/.claude/tiktok/voice.md` if it exists. "Sounds like me" has a reference file, and this
   skill checks against it.
2. Read the draft out loud in your head, line by line. A line you would have to rehearse is a
   line to rewrite.

## The tells, and the fix for each

**Typography**
- Em dashes: delete them. Break the sentence or use a comma. No em dashes in anything you hand
  over, ever.
- Curly quotes and fancy punctuation the user never types: replace with the plain version.
- Double spaces, stray invisible characters, smart apostrophes in the wrong places: clean them.

**The slop lexicon**
These words are how a reader knows a machine wrote it. Delete or replace every one:
delve, tapestry, landscape, realm, elevate, unlock, unleash, foster, furthermore, moreover, in
conclusion, in today's fast-paced world, game-changer, cutting-edge, revolutionary, seamlessly,
moreover, additionally, it is important to note, it is worth noting, as an AI.

**The structural tells**
- "It's not just X, it's Y." Rewrite as one plain claim.
- Rule of three in every paragraph ("fast, fun and free"). Break the pattern or cut two of the
  three.
- A question the text immediately answers. Cut the question or cut the answer.
- "Here's the thing", "Let's dive in", "Buckle up", "Picture this" as openers. Cut them; start
  at the sentence that matters.
- Every sentence the same length. Vary them: one short line, then a longer one.
- A list where a sentence would do. TikTok captions are not bullet points.

**The voice tells**
- A word the user would never say out loud. Check `voice.md`: if it is in the "never say" list,
  it is out.
- A claim the user cannot back up. Flag it, do not soften it into a vaguer claim.
- A joke that explains itself. Cut the explanation, keep the joke, or cut both.

## What to hand back

- the cleaned text in a fenced block, ready to paste
- a short report: how many artefacts stripped, grouped by type (typography, lexicon, structure,
  voice)
- any line you could not fix without changing the meaning, flagged for the user to rewrite

## What this is not

This is a local checklist, not a detector. Never tell the user their text is "undetectable" or
that it "passes AI detection". The point is that it sounds like them, not that it fools a tool.

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
