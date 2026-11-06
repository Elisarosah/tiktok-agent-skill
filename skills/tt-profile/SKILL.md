---
name: tt-profile
description: >-
  Score the user's TikTok profile 0 to 100 across 12 criteria and end in one
  fix. Use whenever the user wants a profile review, "why am I not growing",
  "is my profile good", or a check before a push.
---

# tt-profile

A profile is a promise: the bio says what the next video will be, and the grid proves it. Score the
promise, not the follower count.

## Before you score

1. Read the profile as a stranger would: picture, name, handle, bio, link, pinned videos, last six
   videos. Do not read the analytics first. The stranger does not get analytics.
2. Read `~/.claude/tiktok/log.md` if it exists. What shipped, what the views did. The score is
   about the profile; the log is about the videos.

## The 12 criteria

Score each 0 to 10. Be specific: name the line, the video, the frame.

1. **Picture.** Readable at 40 pixels. One thing, high contrast, no text.
2. **Name.** Says what the account is, not just who runs it.
3. **Handle.** Spellable out loud, no random numbers, matches the other platforms.
4. **Bio, line 1.** One sentence: what you show, for whom. Not a slogan.
5. **Bio, line 2.** The proof: the format, the cadence, the promise.
6. **Link.** One link, and it works. No dead link, no link to nothing.
7. **Pinned videos.** The three best, and they teach a stranger the format in 30 seconds.
8. **Grid coherence.** A stranger scrolling the last nine sees one channel, not nine channels.
9. **Hook consistency.** The first frame of the last six videos each carries a hook, not a logo.
10. **Caption voice.** The captions sound like one person, not a template.
11. **Posting cadence.** The last month shows a rhythm a follower can trust.
12. **Comment presence.** The creator answers questions on their own videos.

## What to hand back

- the score out of 100, with the 12 lines and one sentence each
- the ONE fix, not twenty: the single change that moves the score most this week
- the second fix, labelled as next, so the user knows what comes after

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
