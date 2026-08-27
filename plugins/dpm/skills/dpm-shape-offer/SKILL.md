---
name: dpm-shape-offer
description: Use after a crowd has been researched and scored, to turn it into an offer. Produces the mechanism, the three S, the promise, the pillars, the price and the full ladder, the guarantee, and an evidence bank with a receipt behind every claim. Refuses to shape an offer for a crowd nobody researched.
---

# Shape the offer

The offer is not the product. The product is the files you deliver. The offer is the reason a stranger pays before seeing them. A great product behind a dead offer sells nothing, and the reverse is worse, because refunds hurt.

Everything downstream, the product, the pages, the ads, the price, reads from what this step writes. Budget a session, not ten minutes.

The frame here follows Cole Gordon's compelling-and-scalable offer work, adapted for a low-ticket front end with a ladder behind it. The three S, the mechanism template, the promise-and-pillars shape, and the advantage checklist come from there.

## Refuse to start without the research

Look for `research/RESEARCH-*.md` from `dpm-niche-research` and the score from `dpm-crowd-check`.

If there is no research file, stop and say so. An offer shaped from impressions is a guess with a price on it, and the whole point of the previous step was to stop that happening. Send them back to `/dpm:find-niche`.

If the research exists but scored under 9, say that before you write a word. Shaping a beautiful offer for a crowd that already failed its scorecard is the most expensive mistake available at this stage.

Read the file properly before you open your mouth. The crowd sentence, the verified claims pool, and the quarantine list are all inputs, and you will be held to them.

## Hard limits

**Never invent a number, a result, a customer, or a testimonial.** Not as a placeholder, not as "swap this later." Placeholders ship. Where a line would be stronger with a figure, write `[VERIFY: what figure to go get]` and say what would prove it.

**The quarantine list is off limits.** Anything the research marked `[single-source]` or `[contested]` may shape thinking. It may not appear in the offer, the pages, or an ad.

**Web search and reading pages only. Never drive a browser.** No browser automation, no extension, nothing that takes control of Chrome. Most people running this have no such tool connected, so anything that depends on one cannot be reproduced by the person watching.

**Never work around a block.** When a source sits behind a CAPTCHA, that source is done. Write `could not verify, source blocked` and move on.

**Stay inside the free Apify tier, $5 a month.** Nothing in this skill needs Apify. Do not reach for it.

## Step 1: find out what the market already hears

Run three subagents in parallel. They are independent and each returns a self-contained report.

**A, the promise scan.** Meta Ad Library plus the sales pages behind the ads. For each of five competitors: what result do they promise, do they name a mechanism or only the outcome, and if they name one, is the explanation real reasoning or a label with nothing under it. Are they treating a symptom or a root cause.

**B, the price and ladder scan.** What is already sold to this crowd, at what price, in what format, and what sits above it. Front-end prices, order bumps, upsells, anything recurring. This tells you the band you are entering and what the backend looks like when it works.

**C, the free alternative.** What can this crowd get for nothing today, and exactly where that free advice runs out. This is the most useful of the three, because the gap it finds is where your product lives.

Each prompt ends with the same rule:

> Put a source URL on every factual claim, with the date. Mark anything found in only one place as `[single-source]`. Say "could not verify" rather than filling a gap. Your final message is the deliverable, complete and self-contained, no preamble.

Save the merged result as `research/competitor-mechanisms.md`. Then say plainly what this market is already hearing over and over, which claims are worn out, and where nobody is talking. If all five promise the same thing, say so, because that is the opening.

## Step 2: the interrogation

This is the actual work and it is adversarial. You are a consultant hired to find the flaw, not to encourage anybody.

Ask one question at a time and push back on weak answers. Never send the list.

- What is the approach, step by step? What happens first, second, third?
- Why that order? What breaks if two steps swap?
- What did you add that others do not tell people to do, and why is it critical?
- What did you remove that everyone else includes, and why is it unnecessary?
- What did you combine that is normally done separately?
- Does this fix the root cause or a symptom? Name the root cause.
- Why is your way faster? Why easier? Why more reliable?

Those last three are the honesty gate. If the true answer to all three is "it is not," there is no mechanism yet. Say that. Do not let them name a method they cannot defend, and do not invent an advantage they did not claim.

Watch for the Google check. If the pitch reduces to a tactic somebody can look up in thirty seconds, the product has no pricing power. The fix is never to hide the tactic, it goes inside the product in full. The fix is that the marketing sells the named system and the reasoning, not the loose tactic.

Three kinds of mechanism are legitimate, and it helps to say which one they have:

- **Existing.** A genuinely proprietary sequence. Common in people who have actually done the thing.
- **Unspoken.** Real, everyone in the category does it, nobody says it out loud. A mechanism only has to be new to the buyer.
- **Transubstantiated.** Ordinary steps, made into one system by the naming, sequencing and framing. Most low-ticket products land here and that is fine, as long as the reasoning underneath is real.

The fake fourth kind is an ordinary approach with a cool name and nothing under it. It collapses the first time somebody asks why it is better.

## Step 3: write the mechanism

Six beats, in this order:

> Most people trying to **[get the result]** **[do the common thing]**. The problem with that is **[why it fails]**, which ultimately means **[the consequence they have lived]**. So instead, **[the method]** does **[the specific thing]**, which allows you to **[the benefit]**, which ultimately means **[the benefit behind the benefit]**.

Rules: every claim after "because" has to be reasoning that survives a question. No adjective doing work a specific detail should do. Write three versions with different emphasis, number them, and flag any sentence where you had to invent a fact.

## Step 4: name it, last

Never before you can explain it. The explanation carries the persuasion; the name makes it memorable and makes it theirs.

Two to four words. Says something about how it works, not just the outcome. Search the phrase, and if it is already an established industry term, it is not theirs. Say it out loud, because awkward in the mouth is awkward in an ad.

Give twenty and expect nineteen to die.

## Step 5: the three S

One sentence, three parts: a specific problem, for a specific person, solved a specific way. The specific way is the mechanism, so that part is done.

**Specific problem.** Measurable, with a time frame, something a buyer could answer yes or no on. The test is whether a guarantee could be built around it. Pick the actual bottleneck, not the biggest-sounding outcome. Buyers usually do not doubt the outcome is possible, they doubt they can get the first step to work.

**Specific person.** Life stage, what they already tried and failed at, what they feel bad about, what they can afford. "Women who want a side hustle" is not a person. The failed attempts are what makes it one, because the failed attempts are what the mechanism speaks to.

> Help **[specific person]** get **[specific measurable outcome]** in **[time frame]** using **[mechanism name]**, because **[the one-line reason it works]**.

Stress-test it out loud: is the outcome measurable in thirty days, could a guarantee sit on it, would somebody outside the crowd self-exclude, and is this the real bottleneck. Give three versions with different bottleneck choices and say which one you would bet on.

## Step 6: the one belief

One sentence. The single thing a buyer has to hold before they will buy. Everything on the advertorial and the sales page exists to walk them to it.

> The fastest, lowest-risk way for someone like me, with **[their situation and baggage]**, to get **[outcome]**, is **[mechanism]**, because **[reason one]** and because **[reason two]**.

Write it into `offer.md` near the top. Later, when a section of the sales page is in question, the only question is whether it moves the reader toward this sentence.

## Step 7: the promise

Three parts, and all three have to be things you control.

**Outcome.** What exists at the end that did not exist before. Concrete enough to photograph or point at.

**Container.** How long, and in what shape. A container with no edges reads as vague and converts worse than a shorter one with edges.

**Guarantee.** Two levels, and they want both.

- **The floor.** A plain no-questions refund window, seven or fourteen days. Boring on purpose.
- **The headline guarantee.** Conditional, tied to the three S outcome, with the conditions tied to the specific actions inside the product that make success likely. *Do these two things. If [outcome] has not happened in [time frame], email us, we refund you and you keep everything.*

Conditional works twice: people who do the two things usually get the outcome, so it rarely gets claimed, and naming the two things is itself a sales argument, because it shows how little is being asked.

Never guarantee income. Never promise an outcome you cannot produce. If the offer goes anywhere near money, health, or a guaranteed result, say plainly that the copy needs a lawyer before traffic hits it.

## Step 8: the pillars

Three to five. Each pillar exists to remove one named failure mode, and you should be able to name the failure mode next to it. A pillar that kills nothing is a feature, and features do not sell.

Write them as the buyer's journey through the product, not as a table of contents.

## Step 9: price and the ladder, without being asked

Do this automatically. Nobody has to prompt for it, and an offer without a ladder is the mistake this whole course exists to stop.

**The front end is priced for volume of buyers, not margin.** It buys customers at roughly break-even and hands over a list of people who have proven they will pay. What that list is worth is what the business is worth.

| Price | What it does |
|---|---|
| $7 to $17 | Highest take rate, almost impossible to buy traffic against unless the bump take rate is very high |
| $27 | The default. An impulse decision on a phone, and a bump plus an upsell can carry the ad cost |
| $37 to $47 | More room on ads, slightly fewer buyers. Worth a real test once the proof and the guarantee are real |
| $67+ | Now it is selling, not impulse-selling. Needs proof nobody has on day one |

Start at $27. A higher price is earned by a named mechanism, real proof and a guarantee that means something, never by confidence. When it gets tested, it runs as an arm against a control, not as a replacement.

Then build the whole ladder as a table: slot, name, price, one line, and **the exact deliverable file that has to exist**.

| Slot | Price band | Rule |
|---|---|---|
| Lead magnet | Free | Genuinely useful alone, not a teaser |
| Core | $27 | Carries the guarantee and the mechanism name |
| Order bump | $9 to $27 | Removes a step between them and the outcome. Never "more content" |
| Upsell 1 | $97 to $197 | The done-for-you version of the hardest step in the method |
| Upsell 2 | $17 to $37 | Cheaper, catches the people who said no to upsell 1 |
| Backend | Ongoing | Where the business actually lives |

Two hard rules. **Every row ships on launch day**, so a row with no file path comes off the ladder or gets scoped smaller until it has one. And **no page may promise anything that is not in this table**, with prices matching everywhere they appear, because a mismatch between the sales page and the checkout kills more sales than any headline ever will.

Then compute expected AOV at bump 35%, upsell 1 12%, upsell 2 8%, show the arithmetic line by line, and say what CPA the offer survives at that AOV. Show the same math without the ladder, so the gap is visible. At a $40 CPA a bare $27 product loses $13 a buyer; the same traffic with a bump and an upsell lands near break-even. Three checkbox pages is the whole difference.

Bumps get framed as shortcuts, never as extra reading. The buyer already has too much to read, which is usually why they are stuck.

## Step 10: the advantage, and the evolutionary check

Say plainly why this wins, in the categories that actually hold:

- **A superior way.** The mechanism, if it is real.
- **Superior fulfillment economics.** Produced faster or cheaper than the market can, without hiring.
- **A different buyer.** Selling to someone the competition is not scripting to.
- **Positioning.** Honest proof in a market full of faked receipts is a moat, not a handicap.

Then the evolutionary check, which is a sanity test rather than a section of the sales page: is this model already working somewhere, with the mechanism changed rather than the model? If the answer is that nobody anywhere runs this shape, that is a warning, not an edge.

## Step 11: the evidence bank, without being asked

Write `evidence-bank.md` the moment `offer.md` has claims in it. One row per claim: the claim quoted exactly as written, where it appears, what evidence would prove it, and the status.

Do not guess at sources. Do not soften a claim to make it easier to prove, quote it as written and flag it. `VERIFY` status means the claim does not ship, and it is a launch blocker, not a note.

Then split the rest into three lists: claims that are structurally true of the model and need no receipt, claims that need a screenshot or document before launch, and claims to delete now because they will never be provable. Act on the third list immediately. Deleting an unprovable claim costs almost nothing and takes real risk off the page.

Screenshots live next to the bank. A claim whose receipt cannot be found in ten seconds is not verified.

## Step 12: the line-level test

Run every headline and every promise through three questions before the file closes.

1. **Can a reader picture it?** Zoom in until you hit a physical object. "Get organized" is nothing. "You can find the scissors" is something.
2. **Can it be falsified?** Could somebody check it and find you wrong? Facts land, adjectives do not.
3. **Could a competitor sign their name to it?** If yes, throw it out, you wrote their ad.

Three yeses is a headline. Three noes is filler. The related habit is: do not talk, point. Instead of "affordable," the number. Instead of "fast," the time.

## Write the file

Everything goes in `offer.md` in the project folder, in this order: mechanism, three S, the one belief, the promise, the pillars, the name, price and the full ladder table, the guarantee, the advantage. `evidence-bank.md` sits beside it.

Say the offer back in the three S sentence when you are done, then name the weakest part of it and what would have to be true to fix that. There is always a weakest part, and naming it is more useful than a summary.

## Done state

- `offer.md` exists and holds all nine items
- The mechanism has a written explanation that survives "why is this better," not just a name
- Five competitor promises are on record and the worn-out claims are named
- The three S names a measurable outcome with a time frame
- The one belief is one sentence
- The name was searched and can be owned
- Every ladder row names a deliverable file that can exist before launch day
- Expected AOV is computed and the survivable CPA is stated
- Both guarantee levels are written
- `evidence-bank.md` exists and every row is VERIFIED or flagged as a launch blocker
- Zero invented testimonials, review counts, bylines or badges

When that is true, the next module manufactures the product.
