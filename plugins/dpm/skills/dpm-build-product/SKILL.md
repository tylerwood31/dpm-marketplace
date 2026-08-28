---
name: dpm-build-product
description: Use after the offer is written, to manufacture the product. Turns the ladder table into structured content, a build script, and finished PDFs, rendering the lead magnet and the bump from the same source. Refuses to build for an offer that does not exist, and refuses to draft the whole product before the standard is approved.
---

# Build the product

Write the content once as structured data, then render it into every product on the ladder. The core, the lead magnet and the bump come out of one file, which is why this takes days instead of months.

Two things are true at the same time and you must hold both: **production is fast, and the quality bar does not move.** Fast production and a low bar are separate decisions and the person running this is only making the first one.

## Refuse to start without the offer

Look for `offer.md` and `evidence-bank.md` in the project folder.

If `offer.md` is missing, stop. Send them to `/dpm:shape-offer`. Building a product before the offer exists means manufacturing something nobody decided how to sell, and it gets rebuilt.

If `offer.md` exists but the ladder table has rows with no deliverable file path, say which rows and stop. That table is the build list. A row with no file is not a product, and the fix is one sentence from them, not a guess from you.

Read the whole offer file before you speak. The mechanism, the three S, the price ladder and the evidence bank are all inputs. The mechanism in particular is what the training layer teaches, so if you cannot restate it you are not ready to build.

## Hard limits

**Build exactly what is in the ladder table. Not more.** If they ask to add a module because the product feels thin, say what this skill knows: thin is almost always a packaging problem, not a content problem, and the fix is the countable unit, the annotations and the template layer. Adding explanatory content to a thin product makes it a longer thin product.

**Never draft all the units before the standard is approved.** Five first, then stop. This is a gate, not a suggestion.

**Never invent a claim, a number, a testimonial or a statistic.** The evidence bank governs the product the same way it governs the pages. Anything the research quarantined stays out.

**Do not pad.** If two units make the same point, say so and propose the merge rather than keeping both to protect the count.

## Stage 1: the outline

Conversational, and worth arguing about. The unit count and the field list are decisions they live with for the whole build, because changing the fields later means rewriting every unit.

Work out:

- **The countable unit and the number.** The thing the product contains N of: protocols, plays, scripts, layouts, checklists, prompts. Enough that it is obviously worth the price, small enough to produce at a high standard this week. Justify the number rather than picking a round one.
- **The fields every unit carries.** Identical across every unit, so one template renders all of them.
- **The section groupings**, named the way a buyer would name them, not the way the author would.
- **Front matter and back matter.** Cover, how to use this, anything needed before unit one.
- **Which five units become the lead magnet**, and why those five.

Every unit must be immediately usable. If a unit is only theory, cut it or attach an action to it.

Time-scope it as well as counting it. "Sixty protocols" is a claim about volume; "sixty seconds each" is what tells a buyer they can actually do it. Volume without time-scoping reads as homework.

## Stage 2: the content file, with a gate

Write `content.json` with the agreed fields. Fill in **five entries only**, completely, as examples of the standard.

Rules for every entry:

- Every step is a physical action someone could take without deciding anything. "Plan your week" is not an action. "Open the calendar and block Tuesday 9am" is.
- The "why this works" line is reasoning, not encouragement.
- No entry repeats the core idea of another.
- Second person, short sentences, no adjective doing work a specific detail should do.
- One line per unit saying why it exists for this specific buyer. That annotation habit is worth more to perceived value than any design work, and it proves the mechanism over and over through the product.

**Then stop and make them read the five.** Do not continue to unit six on your own initiative. When they approve the standard, draft in batches of ten and stop after each batch. Tell them to read the batch. This is the part where a product gets good or gets padded, and an unattended run produces units that are individually fine and collectively identical.

If they have a voice skill built from `dpm-voice`, use it here. Sixty units in generic model voice is the thing a buyer notices first and trusts least.

## Stage 3: the build script

One script reads `content.json`, writes a print-ready HTML document, and renders it to PDF.

Requirements to build to:

- One shared stylesheet. US Letter, zero page margin with padding in the page class so it stays controllable, `page-break-after` on every page block, background printing forced on.
- Colours as CSS variables at the top, so the palette changes in one place. Each section grouping gets its own accent through a variable, so one page template serves every section.
- Page types: cover, contents, how-to-use, one divider per section, one page per unit, closing page.
- Contents links to each divider, each unit links back to contents, and the links survive into the PDF.
- Headless Chromium, print media emulation, backgrounds on.
- Print the page count when it finishes.

Expect to iterate for an hour. That is normal and it is the last time this script gets touched for this product.

## Stage 4: check the render, honestly

Run it, then report three things without being asked:

1. **Overflow.** Did any unit page spill onto a second page. Overflow is what makes a generated document look amateur, and the fix is either capping content length per unit in the data or reducing the type size.
2. **Colour.** Did the backgrounds actually print, or did the browser strip them.
3. **Links.** Do the internal links work in a real PDF reader, not just a browser preview.

Tell them to open the finished file the way a buyer will. You cannot check that part for them.

## Stage 5: the rest of the ladder, without being asked

This is the payoff and it is the step people skip, which is how a ladder ends up half built with three rows and one file.

Once the build script exists, extend it. Same `content.json`, same stylesheet, same unit template:

- **The lead magnet.** Only the five chosen entries, renumbered 01 to 05 so they read as a set rather than a sample. Its own cover, and a closing page that names what the full product contains, lists the section groupings with one line each, and says where to get it.
- **The bump.** Same data, different selection, different layout, separate output.
- **Preview images.** PNGs of the cover, the contents page and four representative unit pages from different sections, at 2x, into `assets/previews/`. These are renders of the real document, never mockups, which means the sales page can show actual pages and say so.

Do all three as a matter of course. They are nearly free once the script exists, and each one is a row on the ladder that otherwise stays empty.

## Stage 6: the refund audit, twice

Run it without being asked, as a buyer who paid and is deciding whether to refund, not being polite.

Flag: any two units making the same point, any unit whose steps leave a decision to the reader that the product should have made, any "why this works" line that is a pep talk, any unit obvious enough to feel like a cheat, and anywhere the product explains for more than three paragraphs before telling the reader to do something.

Then answer one question directly: **could the buyer do something useful within ten minutes of opening this?** If not, name what is blocking them.

Fix what it finds and run it again. The second pass always turns up what the first pass hid.

The one to hold the line on: if deleting a unit entirely would not make the product worse, it goes. A tighter product with an honest count beats a padded one with an impressive count, and the padded version is what generates refunds. Nobody has ever praised a product for being long.

## Packaging

The buyer sees the filenames, so name them like a product. `[Mechanism Name] — The Complete System.pdf`, not `final_v3_REAL.pdf`. Folders numbered in the order they should be opened, and a one-page START HERE at the root when there is more than one file.

Then say the version rule out loud, because it decides whether the pipeline was worth building: the source is the content file, the build script and the stylesheet. A typo gets fixed in the content file and rebuilt. Fixed in the PDF, the next rebuild silently reverts it.

## Done state

- Every ladder row has a deliverable file path and every one of those files exists
- The content file holds every unit with the same fields on each
- One command produces the core product PDF
- The same command produces the lead magnet, with its own cover and closing page
- Page count, internal links, colours and overflow all checked on the real file
- Every unit has a "why this works" line that is reasoning
- The refund audit ran at least twice and what it found was cut
- A buyer could do something useful within ten minutes
- Preview images are rendered from the real document
- Files are named like products, with a START HERE if there is more than one
- The source is saved so it can be rebuilt after a fix

When that is true there is something to sell, and the next step is the machine that takes the money.
