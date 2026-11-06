---
name: tt-repurpose
description: >-
  Turn one posted video into a week of content: new hooks, new captions, new
  angles, new formats. Use whenever the user wants more from a video that
  worked, "turn this into more posts", or a week without a new shoot.
---

# tt-repurpose

One good video is three to five posts, if you cut it right. The mechanism does not change; the
door into it does.

## Before you cut

1. Watch the video, or read the script. The repurpose starts from what is actually in it, not
   from the idea of it.
2. Read `~/.claude/tiktok/log.md` if it exists. A video that already worked earns the repurpose;
   a video that flopped earns an autopsy from `/tt-profile` first.

## The cuts

| cut | what changes | what stays |
| --- | --- | --- |
| **New hook** | Same video, new first 3 seconds: a different formula from [the 18](../tt-script/hooks.json), new on-screen line | Everything after the hook |
| **New caption** | Same video, new first line and new hashtags for a different search | The video, the keyword |
| **The zoom-in** | One beat of the video, alone, as its own 15 second post | The mechanism, the payoff |
| **The question** | The most asked comment, answered as its own video | The format, the voice |
| **The cross-post** | Same video, new hook and caption for Shorts or Reels | The render, the mechanism |

- **One change per cut.** A repurpose that changes the hook, the caption and the format at once is
  a new video, and you cannot tell what worked.
- **The best video earns the most cuts.** Repurpose the outlier first. A 10x video deserves five
  cuts; a 1x video deserves one.
- **Never repost the identical video the same week.** The algorithm has seen it. The audience has
  seen it. Change the door, not the room.
- **Each cut names its hook formula.** Run the new hook through `/tt-script` before you call the
  cut done.

## What to hand back

- the five cuts as a table: cut, new hook, new caption line, where it posts
- the order to ship them, best first
- one line per cut saying what changed and what did not

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
