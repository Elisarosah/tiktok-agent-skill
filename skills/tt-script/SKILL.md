---
name: tt-script
description: >-
  Write a TikTok video script from a raw idea - hook options off 18 formulas
  built for the 1 to 3 second TikTok hook, scored, then the full spoken script
  with the beats timed. Use whenever the user wants a TikTok script, a hook, an
  opening line, "what should I say", "write my next TikTok", or is about to
  record and does not have the first second yet.
---

# tt-script

One idea into a script somebody finishes.

Two tools live in this folder and both actually run. Use them. Do not eyeball the hook.

```bash
python3 hookscore.py hooks.txt              # rank your hook options
python3 hookscore.py --hook "one line"      # score a single one
```

## Before you write

1. Read `~/.claude/tiktok/voice.md` if it exists. That is the user's voice profile: how they talk
   on camera, the words they never use, who they are talking to, what they will not claim. If it
   does not exist, ask for **three of their own videos**, read or transcribe them, infer the voice,
   and write the file. A script in the wrong voice is worse than no script, because they have to
   read it out loud.
2. Never invent a number, a result or a source. If a figure would strengthen it and you do not have
   one, ask for it or write the line without it.
3. If `~/.claude/tiktok/swipe.md` exists, read it. `/tt-viral` writes that file, and it is the
   user's own evidence about which formulas are working in their niche right now. It beats the
   defaults in this file.

## The shape

A TikTok is decided in the first second and kept by the next five. The hook is 1 to 3 seconds,
5 to 12 spoken words, and it does two things or the video leaks: stop the thumb, and open a
question the viewer cannot close.

```
0:00 - 0:03   HOOK        the claim. Spoken line and on-screen line, written
                          separately. Motion in the first frame, never a static image.
0:03 - 0:08   THE STAKE   why this matters to the person watching. One line.
0:08 - ...    THE BODY    one idea per beat, and the frame changes every beat.
LAST 3s       THE PAYOFF  deliver what the hook promised, then the single ask.
LAST LINE     THE LOOP    echo one word from the hook so the replay lands clean.
```

Length: 15 to 45 seconds is the working range for a teardown. Under 15 seconds the loop counts
inflate and nothing else does. Over 60 seconds the video needs a second hook at the middle.

## The loop

**1. Pick three hooks, not one.** Run the idea through `hooks.json`, choose three formulas that
genuinely fit it, and write the spoken line plus the on-screen line for each. Different formulas,
not three rewrites of one.

**2. Score them.** Put the three spoken lines in a file, one per line, and run `hookscore.py`.
Show the user the ranking. If the top one is under 50, you do not have the hook yet and no amount
of editing fixes that. Note the scores run lower here than on YouTube, because a 1 to 3 second hook
has less room for all five properties: use the ranking between the options and the weakest-property
fix, not the absolute band.

**3. Write the script** on the winning hook. Plain spoken language, the way the user actually
talks. Contractions. Short lines. No sentence they would have to rehearse. For a faceless teardown,
every beat names what is ON SCREEN: the animation shows the mechanism, the voice explains it.
Say "receipt", show the receipt.

**4. Time it.** Estimate at 150 words per minute for voiceover. Flag every beat over 4 seconds
and every stretch with nothing concrete on screen. A static shot for 8 seconds is where people
leave.

**5. Humanize it.** Run the script through `/tt-humanizer` before showing it. A written-sounding
line is obvious the moment someone says it out loud.

**6. Print the block.** The script in a fenced block, the on-screen text as a separate list with
timings, and then:

```
SCRIPT READY
hook:       #1 The Impossible Inside, scored 58 WORKABLE
length:     28.4s across 9 beats at 165 wpm
on-screen:  6 cards
humanizer:  3 artefacts stripped
caption:    run /tt-caption next

Reply "yes" to log it, or tell me what to change.
```

**7. Never publish.** This skill produces a script. The user shoots it and posts it. On "yes",
append to `~/.claude/tiktok/log.md` with the date, the hook formula used and the first line, so
`/tt-profile` has a history later.

## On-screen text is a separate script

Write it separately, every time. It is read before it is heard.

- **Six words or fewer per card.** It is being read at arm's length by someone who is not
  listening yet.
- **The hook card is up at frame 1**, not after a beat of silence.
- **Keep it inside the safe zone.** On a 1080x1920 frame, nothing above y=230 or below y=1440,
  and keep the right 230 pixels clear. The interface sits on top of everything outside that box:
  the caption, the action rail, the audio strip.
- **Never put the hook where the caption sits.** That is the bottom of the frame and it is covered.
- **Burn in captions for the body.** Most people watch muted first.

## Rules that make the difference

- **One idea per video.** If the script has two, you have two videos. Say so.
- **Numbers over adjectives.** "$4,200" beats "a lot". If the user has not given a number, ask for
  one rather than writing around the hole.
- **Cut the intro.** No greeting, no "in this video", no name, no logo sting. The video starts at
  the sentence you would normally reach at second six.
- **Change the frame every beat.** A static shot for 8 seconds is where people leave.
- **One ask at the end.** Comment a keyword, save it, or follow. One.
- **Never fabricate.** No invented metrics, clients, revenue or outcomes under the user's name,
  even as a placeholder. If a number is needed and unknown, leave `{{your number}}` in the script
  and flag it.
- **Do not write a script around a trending sound the user cannot use.** If the idea needs the
  user's own voice, say so.

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
