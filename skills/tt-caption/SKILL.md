---
name: tt-caption
description: >-
  Write a TikTok caption and hashtags as one pairing, with the first line
  carrying the ask past the "more" cut. Use whenever the user wants a caption,
  hashtags, "what should the caption say", or is about to post and the caption
  is blank.
---

# tt-caption

The caption is not the script. It is the second hook, the ask, and the search terms, in that order.

## Before you write

1. Read `~/.claude/tiktok/voice.md` if it exists. The caption has to sound like the same person as
   the voiceover, or the post feels stitched together.
2. Read the script or the video first. A caption written without the video repeats the hook instead
   of adding to it.

## The shape

```
LINE 1   the ask. The one action, in the first 100 characters, so it survives the "... more" cut.
         Comment KEYWORD, save it, or follow. One ask, same as the video.
LINES 2-4  two to four short lines with the words people search. The mechanism, the object, the
         surprise. No links, TikTok does not make them clickable here.
HASHTAGS   3 to 5 specific ones. The niche, the object, the format. Never #fyp, #viral,
         #foryou, #explorepage: they signal nothing to the algorithm and everything to a human.
```

- **Line 1 is the ask, not the summary.** The viewer already watched the video. The caption tells
  them what to do next.
- **Say the keyword out loud in the video and write it in line 1.** The comment keyword is one
  word, and it is the same word in both places.
- **Hashtags are search terms, not decoration.** If the hashtag would not be a search query, cut
  it. Three specific tags beat eight vague ones.
- **No links in the caption.** Put the link in the bio and say so, once, only when there is
  something to send.
- **Match the video's claim exactly.** If the video says "inside your earbuds", the caption does
  not say "inside your headphones". One object, one name, everywhere.

## What to hand back

- the caption in a fenced block, ready to paste
- the hashtags on their own line
- one line naming the keyword and where it appears (spoken, on screen, caption line 1)
- if the caption is for a video in another language, write that version too, with the same keyword
  translated only if the audience expects it

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
