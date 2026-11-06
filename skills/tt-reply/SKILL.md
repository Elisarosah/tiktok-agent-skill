---
name: tt-reply
description: >-
  Triage the comments on the user's own videos into piles, then write replies
  in their voice. Says which one to pin. Use whenever the user wants help with
  replies, "what should I answer", or a comment section that needs tending.
---

# tt-reply

The comment section is where a viewer becomes a follower. Replying well is the cheapest retention
work on the channel, and replying to everything is how a small channel dies. Triage first.

## Before you write

1. Read the comments, all of them if the video is small, the top 30 if it is big.
2. Read `~/.claude/tiktok/voice.md` if it exists. Replies have to sound like the same person as
   the voiceover.

## The piles

Sort every comment into one of four piles. A comment goes in one pile only.

| pile | what it is | what to do |
| --- | --- | --- |
| **Questions** | A real question about the mechanism, the object, the video | Answer it. Short, with the fact. This is the content. |
| **Praise** | "Love this", "so cool", an emoji | Like it. Reply only if the reply adds a fact. A like is an answer. |
| **Skeptics** | "That is wrong", "fake", "source?" | Answer once, with the fact or the source. Never argue twice. |
| **Spam** | Links, "follow me", crypto, the same text on every video | Delete or ignore. Never reply. A reply feeds it. |

## The rules

- **Answer questions first.** They are the next video's topic list. If three people ask the same
  thing, say so: that is the next script.
- **One line per reply, usually.** A paragraph in your own comments is a second video nobody
  asked for.
- **Pin the best question.** The pinned comment should be the question the most people are
  thinking. Say which one to pin and why.
- **Reply as a video when the question deserves it.** If the answer needs a mechanism on screen,
  do not type it: flag it as a video reply and hand it to `/tt-script`.
- **Never automate the sending.** This skill writes the replies. The user posts them from their own
  account. Automated replies violate TikTok's terms and read as spam the moment one lands wrong.
- **Never invent a fact to win an argument.** If you do not know, say so and promise the follow-up.

## What to hand back

- the four piles, with counts
- the replies, each under the comment it answers, in a fenced block
- which comment to pin, and why
- the questions that repeat, as next-video topics

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
