---
name: tt-plan
description: >-
  Build a posting week that fits the hours the user actually has: one main
  video, one quick one, one remix. Use whenever the user wants a content plan,
  a posting calendar, "what should I post this week", or a schedule that
  survives a busy week.
---

# tt-plan

A plan that needs ten free hours is a plan that does not happen. This one fits the hours the user
actually has.

## Before you plan

1. Ask how many hours this week, for real. Not the aspirational number.
2. Read `~/.claude/tiktok/log.md` if it exists. What shipped last week, what the views did, which
   hook formula won. The plan builds on evidence, not on a blank page.
3. Read `~/.claude/tiktok/swipe.md` if it exists. `/tt-viral` writes it, and it says which
   formulas are working in the niche right now.

## The week

Three posts is the default. One main, one quick, one remix. That is the whole week.

| slot | what | time to make |
| --- | --- | --- |
| **Main** | One teardown, the full pipeline: `/tt-viral` idea, `/tt-script`, render, `/tt-caption` | the bulk of the hours |
| **Quick** | One idea, one mechanism, one shot. A single surprising fact with the animation to prove it | under an hour |
| **Remix** | A posted video cut a new way: new hook, new caption, new first frame. Run `/tt-repurpose` | under an hour |

- **One idea per video.** If a slot has two ideas, it is two slots. Say so.
- **The main video gets the best idea.** Do not spend the best hook on the quick slot.
- **Leave one slot empty on purpose.** A week with no slack is a week that slips. The empty slot
  is for the trend that shows up on Wednesday.
- **Post when the audience is awake, not when the video is done.** If the render finishes at 2am,
  it waits for the morning slot. Say the slot in the plan.
- **Every slot names its hook formula and its keyword before anything is written.** A slot without
  a hook is a slot that will eat the whole afternoon.

## What to hand back

- the week as a table: day, slot, topic, hook formula, keyword, hours
- the total hours, next to the hours the user said they have
- one line per slot saying what "done" means (script ready, rendered, posted)
- the empty slot, labelled as the flex slot

## The gate

Nothing here publishes. This skill writes and you publish. Every output ends in a block the user
copies, and the last line of every run is the question: **ship it, or change it?**
