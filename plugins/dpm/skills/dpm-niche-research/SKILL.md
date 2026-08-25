---
name: dpm-niche-research
description: Use when the user has a candidate niche or crowd and wants it researched before building anything. Runs four parallel research tracks, enforces source discipline, and produces an evidence file that dpm-crowd-check can score. Refuses to invent a niche out of nothing.
---

# Niche research

Four research tracks, run in parallel, against **one candidate crowd at a time**. Output is an evidence file with a URL on every claim. That file is what `dpm-crowd-check` scores, and later, what ad copy is allowed to draw from.

## First: you cannot generate the candidate

If the user says "find me a starving crowd" with nothing attached, do not produce a list. A model asked to invent niches returns the same plausible, saturated, unverifiable set every time (meal prep, notion templates, dog training), and building on that is how people waste a month.

Push back once, and ask for one of these instead:

1. **Something they saw.** A flyer, a sign, an argument at work, a subreddit that will not stop growing, a problem a friend keeps complaining about. Physical-world observation beats anything a model produces, because it is evidence nobody else has read yet.
2. **Something they already know.** A hobby, a job, a thing they have already solved for themselves.
3. **A trend they noticed but do not understand.** This one is often the best. Not understanding it is fine, the research fixes that.

Then take that candidate and run everything below on it. The model's job is to kill or confirm a candidate, not to dream one up.

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

## Then score it

Hand the evidence file to `dpm-crowd-check` and score the candidate against the 8 conditions. The score is only as good as this file. A candidate scored from impressions instead of sources is a guess wearing a number.

Research three candidates before committing to one. Expect at least one to fail. A track that comes back thin is a result, not a setback.
