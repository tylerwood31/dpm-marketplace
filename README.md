# The Digital Product Machine

Skills and MCP servers for building and selling a one-person digital product business with Claude Code.

## Install

```
claude plugin marketplace add tylerwood31/dpm-marketplace
claude plugin install dpm@dpm
```

That's it. Two commands, and it installs six skills plus the MCP servers they rely on.

Needs Claude Code, which needs a paid Claude plan (Pro or above). The free plan does not include it.

## Where to start

Once it's installed, type this and hit enter:

```
/dpm:find-niche
```

It asks what you've got, works it into a specific group of people with a specific problem, and then goes and finds out whether that group is real. You don't need an idea ready. It'll ask.

When that comes back scored, the next one turns the crowd into something you can sell:

```
/dpm:shape-offer
```

And when the offer is written, the third one manufactures the product:

```
/dpm:build-product
```

## What you get

**dpm-niche-research** starts as a conversation. You bring interests, it works them into a specific crowd with a specific problem, then runs four research tracks on that at once, so you find out whether the crowd is real, what they're angry about, whether there's actually a product in it, and whether anyone's already selling to them. Every claim comes back with a source, and anything it couldn't verify gets quarantined so it never ends up in an ad.

**dpm-shape-offer** takes the crowd you researched and builds the offer around it: the mechanism that says why your way works when the last four things they tried didn't, the one sentence that names the person and the problem, the promise, the price, and the whole ladder behind the price. It won't run on a crowd you haven't researched, and it writes an evidence bank so every number on your sales page has a receipt you can find. The frame follows Cole Gordon's compelling-and-scalable offer work, adapted for a low-ticket front end.

**dpm-build-product** turns the offer into the thing you actually hand over. It writes your content once as structured data, builds a script that renders it into a print-ready PDF, and then produces the lead magnet, the order bump and the sales-page preview images from that same file, so the whole ladder comes out of one source instead of three separate builds. It will not draft your entire product before you have read the first five entries and approved the standard, because unattended drafting is how you end up with sixty units that are individually fine and collectively identical.

**dpm-crowd-check** scores a niche against eight conditions and refuses to score one you haven't actually researched. Guessing at this is the reason most people build things nobody buys.

**dpm-ad-policy** builds you an evidence log of what your ad account actually gets approved and rejected for, instead of guessing at rules the platforms don't publish. Your approved ads are the evidence.

**dpm-voice** builds a personal voice skill from writing you've already done, so what you publish sounds like you rather than like everyone else using the same tools.

## MCP servers

**context7** is free and needs no account. It pulls real, current library documentation so Claude stops inventing functions that don't exist. If you install nothing else, install this.

**apify** scrapes Reddit and marketplaces at volume, for when reading threads by hand gets old. The free tier is $5 of credit a month with no card required, which covers several deep research runs. It will say "needs authentication" until you connect it. That is normal and nothing is broken.

## Where this came from

These are the tools behind [The Digital Product Machine](https://thedigitalproductmachine.com), a written build for a one-person digital product business. The course shows you how to use them and why each one exists. The Stripe account behind it is on the site, the good months and the month it fell 91 percent.

The skills work fine on their own. They just make more sense with the reasoning attached.
