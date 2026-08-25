---
name: dpm-voice
description: Use to build a personal voice skill from your own writing, then to rewrite anything you are about to publish so it sounds like you. Generic "human" writing still reads as AI; this makes it read as you specifically.
---

# Your voice, not a human voice

Stripping AI tells gets you to neutral. Neutral still is not you. This builds a reusable voice skill from writing you have already done, then applies it.

## Step 1, gather real samples

Collect 5 to 10 things you actually wrote and sent. Emails, posts, replies, DMs. Not things you drafted carefully for an audience you were trying to impress. The ordinary ones are better evidence.

Do not skip this and describe your voice from memory. People describe a voice they wish they had.

## Step 2, extract the pattern

From the samples, write down:

- **Sentence rhythm.** Where are the short ones. Do they run long and then stop hard.
- **Words you actually use** and words you never use. Both matter.
- **How you open.** Straight into it, or a beat of context first.
- **How you handle being wrong or unsure.** This is the most individual thing anyone does.
- **Punctuation habits.** Dashes, semicolons, sentence fragments, one-line paragraphs.
- **What you refuse to do.** Hype words, exclamation points, hedging.

Quote a real line from the samples as evidence for each. A trait with no quote behind it is invented.

## Step 3, write it as a skill

Save as `~/.claude/skills/my-voice/SKILL.md` with the traits, the banned list, and three before-and-after pairs taken from real edits.

## Step 4, use it on everything outbound

Run it last, after any generic cleanup, and re-run it after every edit. An edit made to fix one problem routinely reintroduces another.

Then check mechanically, because the eye misses these:

- Count em dashes. More than one in a short piece reads as machine-written to most people.
- Check line lengths. Prose should be one long line per paragraph. A run of similar-length lines means it was hard-wrapped, which renders as ragged text in email clients.
- Read the opening sentence alone. If it could open anyone's message, rewrite it.

## The test

Put the result next to a real sample. If you cannot tell which is which, it is done. If the new one is smoother, it is not done, it is generic. Smoother is usually worse.
