---
name: dpm-niche-research
description: Use when picking or researching a niche for a digital product, including when the user only has vague interests. Reframes an interest into a specific crowd through conversation, then runs four parallel research tracks and produces a sourced evidence file that dpm-crowd-check can score. Refuses to invent a niche out of nothing.
---

# Niche research

Four research tracks, run in parallel, against **one candidate crowd at a time**. Output is an evidence file with a URL on every claim. That file is what `dpm-crowd-check` scores, and later, what ad copy is allowed to draw from.

## Start with a conversation, not a form

Most people arrive with interests, not crowds. "I like hiking." "I've done a lot of home renovation." "I'm into personal finance." None of those are crowds, and none of them can be researched as written. The work at this stage is reframing, and it is a conversation, so hold it like one. **Ask one question at a time and react to the answer.** Do not send a numbered list of questions and wait. That turns a useful ten-minute talk into homework nobody finishes.

If they arrive with nothing at all, do not generate niches for them. A model asked to invent a starving crowd returns the same plausible, saturated, unverifiable set every time, and none of it can be checked. Ask instead for one of three things:

1. **Something they saw.** A flyer, a sign, an argument at work, a subreddit that keeps growing, a problem a friend will not stop complaining about. Physical-world observation beats anything a model produces, because nobody else has read it yet.
2. **Something they already know.** A hobby, a job, a thing they solved for themselves once.
3. **A trend they noticed and do not understand.** Often the best one. Not understanding it is fine, that is what the research is for.

### Turning an interest into a crowd

An interest is a doorway, not a crowd. You stand inside it and look for the specific person who is stuck. Work toward three things, in this order:

**Who, specifically, and what do they call themselves.** "People interested in hiking" is not a crowd. "People who just adopted a rescue dog that pulls" is. Push for a name they would use for themselves, because that name is what you will search for later.

**What just happened to them.** Almost every real crowd is defined by a recent event, not a standing interest. A diagnosis, a move, a baby, a layoff, a purchase they now regret, a season with a date on it. The event is what creates urgency, and urgency is the difference between someone who reads and someone who buys. If you cannot name the event, keep digging, you are still describing a topic.

**What they have already tried and paid for.** If the answer is nothing, that is a warning. People who have never spent money on a problem usually do not start with you.

Offer reframes, do not just interrogate. If somebody says "personal finance," it is more useful to say "so is it people who just got their first real salary and have no idea what to do with it, or people staring down a mortgage renewal at a rate that doubled?" and let them pick, than to ask them to narrow it themselves. Two or three concrete reframes will move them further in a minute than five open questions.

Then say plainly which reframe you would research and why, and let them overrule you. They know things about the crowd that you do not.

### Before you spend the research

Read the candidate back in one sentence, in this shape:

> **[who they are], who just [the event], and are currently [what they are doing about it badly].**

If that sentence is hard to write, the candidate is not ready and no amount of research will fix it. If they have three candidates, write three sentences and research all three. Expect at least one to die, and say so up front, because a person who expects a candidate to fail keeps going when one does.

## Hard limits on how you research

These are not preferences. Breaking them either costs the person money or leaves them watching something they cannot reproduce.

**Web search and reading pages only. Never drive a browser.** Do not use browser automation, a browser extension, or any tool that takes control of Chrome. Most people running this have no such tool connected, so a research run that depends on one cannot be repeated by the person watching. Plain search and page reads are the whole toolkit.

**Never work around a block.** Etsy, Facebook and others sit behind CAPTCHAs and bot protection. When a source blocks you, that is the end of that source. Do not try to bypass it, do not hunt for another route in, and do not ask the person to fetch it for you. Write `could not verify, source blocked` and move on. A gap recorded honestly costs nothing, and four tracks still come back with plenty.

**Stay inside the free Apify tier, which is $5 a month.** The course tells people this step is free and that promise has to hold. So:

- Do not touch Apify during the four tracks. Nothing in them needs it.
- Use it only when the person explicitly asks to go deeper on Track 2, after the four tracks are in, and only to pull one subreddit at volume.
- One run per candidate at most. Say what it will cost and get a yes before running it.
- Never run an actor speculatively, never run one to see what comes back, and never run several at once.

If Apify is not connected or its credits are gone, the research still runs. It reads fewer threads on the sentiment track. Say that plainly rather than stopping.

## The four tracks

Launch all four as parallel subagents. Each is independent and each returns a self-contained markdown report. Substitute the crowd, the problem, and the product shape being tested.

Every track prompt ends with the same evidence rule, so paste it into all four:

> Put a source URL on every factual claim, with the date. Mark anything you found in only one place as `[single-source]`, and anything sources disagree on as `[contested]`. Say "could not verify" rather than filling a gap. Your final message is the deliverable, complete and self-contained, no preamble.

**Track 1, experts and institutions.** What do the serious people say about this problem? Trade bodies, researchers, regulators, journalists, lawsuits, published data. Scale of the problem, who is affected, what is documented rather than felt. This track tells you whether the problem is real or just loud.

**Track 2, public sentiment.** How do ordinary people talk about it. Subreddits and their subscriber counts, Facebook groups, the recurring complaints, the exact phrases they use. Pull representative quotes with the thread they came from. Note whether the crowd holds together or splits into factions, and note the words they use for themselves. This track gives you the ad copy later.

**Track 3, the solution landscape.** What can somebody actually do about this problem today, and where does the advice run out. Free tools, existing how-tos, the parts everyone gets wrong, the boundaries you must not cross (legal, medical, financial). **This track is the product spine.** If it comes back thin, there is no product, no matter how angry the crowd is.

**Track 4, market and ad viability.** Who is already selling into this crowd. For each: price, format, how long they have been at it, and what they are missing. Demand direction over the last two years. Then the ads question, which is the one people skip: search the Meta Ad Library for the closest advertisers, note how long their ads have run, and check whether this category triggers a restricted policy (health claims, financial claims, social issues, employment). A crowd you cannot legally advertise to is not a crowd you can buy customers from.

## Then a fifth pass, always

The four tracks come back with holes. Run one follow-up agent on the specific gaps: an unverified number, a competitor whose price you could not find, a policy question left open. Ask it to close those and only those. Research that never gets a second pass stays at about eighty percent, and the missing twenty percent is usually the part that decides it.

## Write the evidence file

Compile everything into one dated file, `research/RESEARCH-<date>.md`, with the tracks kept separate and a **verified claims pool** at the bottom.

The pool has two lists: claims with a live source URL that copy may use, and a **quarantine list** of everything marked `[single-source]` or `[contested]`. Quarantined claims may inform your thinking. They may never appear in an ad, a sales page, or the product. Write that rule into the file itself, because the person writing copy in three weeks will not remember it.

## Then score it, without being asked

Scoring is the last step of this skill, not a separate request. The moment the evidence file is written, hand it to `dpm-crowd-check` and score the candidate against the 8 conditions. Do not stop and wait to be prompted, and do not ask whether they want it scored. They ran this to find out whether the crowd is worth building for, and an unscored evidence file does not answer that.

Say the total and the verdict in plain words, then the conditions that scored lowest and what would have to be true to move them.

The score is only as good as the file underneath it. A candidate scored from impressions instead of sources is a guess wearing a number.

Research three candidates before committing to one. Expect at least one to fail. A track that comes back thin is a result, not a setback.
