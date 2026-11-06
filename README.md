# The TikTok agent skill

Nine Claude skills that run a TikTok account. Free, MIT, no signup, no API key, nothing to
connect.

One of them writes your script off 18 hook formulas built for the 1 to 3 second TikTok hook and
scores the hook before you waste a take on it. One finds what is working in your niche and ranks it
by how far each video beat its own creator, not by how big the creator is. One writes the caption
and the hashtags as a pair, because a caption written separately from the hook is why half of your
posts bury the ask. One turns one video into a week of content. One strips the AI fingerprint off
your text before anything ships.

**Nothing gets published until you do it.** These skills write. You upload.

## Install

This pack lives in a folder, not on GitHub yet, so install it by copying the
skills into Claude Code:

```bash
cp -r tiktok-agent-skill/skills/tt-* ~/.claude/skills/
```

Project-local instead of global: copy the same folders into your repo's `.claude/skills/`. No Claude
Code at all? Paste any single `SKILL.md` at the top of a chat and it runs as a mode. You lose the
two Python tools, which is most of the point of `/tt-script` and `/tt-viral`, but the rest works.

If the pack gets a GitHub repo later, the plugin files in `.claude-plugin/` make it installable
as a plugin:

```
/plugin marketplace add <owner>/tiktok-agent-skill
/plugin install tiktok-agent
```

Then spend ten minutes on [`templates/voice.md`](templates/voice.md). Copy it to
`~/.claude/tiktok/voice.md` and fill it in, or send Claude three of your own videos and say "write
my voice.md from these". Every skill reads that file. It matters more here than anywhere else,
because you have to say the words out loud and the hook is one second long.

## The nine

| command | what it does |
| --- | --- |
| `/tt-script` | One idea into a script. Three hooks off [18 formulas](skills/tt-script/hooks.json) for 1 to 3 second hooks, scored, then the spoken script with the beats timed. |
| `/tt-caption` | Caption and hashtags as one pairing, with the first line carrying the ask past the "more" cut. |
| `/tt-viral` | What is working in your niche, ranked by multiple over each creator's own median. |
| `/tt-plan` | A week that fits the hours you actually have. One main video, one quick one, one remix. |
| `/tt-comment` | Comments on other creators' videos: add value in the niche, never spam, never cold-pitch. |
| `/tt-reply` | Your own comments triaged into piles, then replies in your voice. Says which one to pin. |
| `/tt-profile` | Your profile scored 0 to 100 across 12 criteria, ending in one fix. |
| `/tt-repurpose` | One video into a week of content: new hooks, new captions, new angles. |
| `/tt-humanizer` | Strips the AI fingerprint off a script or caption before it ships. |

## The two tools

Both run on a clean Python 3 with no dependencies. They are the reason the skills are
not just prompts.

```bash
python3 skills/tt-script/hookscore.py --hook "one line"   # 5-property hook panel
python3 skills/tt-viral/swipe.py collected.json --min 2.0  # outliers by own-creator multiple
```

## The fine print

- **Nothing here logs in, posts, comments, follows or DMs.** The tools write; you publish. TikTok
  has no official posting path in this pack on purpose.
- **The hook score is a heuristic, not a prediction.** `hookscore.py` is adapted from Jake
  Schincariol's scorer, which was calibrated on 74 real short-form hooks: it separates
  deliberately bad hooks from real ones well (AUC 0.83 in his calibration) and a creator's hits
  from their own misses barely at all (AUC 0.56). The brevity band here was changed for TikTok's
  1 to 3 second hook, so treat a low score as a reason to look again, never a high score as a
  promise of views.
- **Outlier multiples from a hand-collected batch are evidence, not proof.** Formats decay;
  re-run `/tt-viral` monthly.
- **Never invent a number, a result, a client or a source.** If a figure would strengthen a
  script and you do not have one, ask for it or write the line without it.

## Credits

Derived from two MIT-licensed packs by Jake Schincariol:
[youtube-agent-skill](https://github.com/Jakeschincariol/youtube-agent-skill) (the hook scoring
panel, the 21-formula library, the swipe ranking) and
[instagram-agent-skill](https://github.com/Jakeschincariol/instagram-agent-skill) (the short-form
script shape, the caption rules, the humanizer). The hook formulas were rewritten for TikTok's
1 to 3 second hook and for a faceless teardown channel. MIT. Use it, change it, ship it.
