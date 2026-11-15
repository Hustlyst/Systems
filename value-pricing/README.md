# Value Pricing

Price your next project from what it is worth to the client, with the maths shown, three options to choose from and a floor you never go below.

Pricing by hours times a day rate caps what you earn and invites clients to compare you on rate. Value Pricing reads your discovery notes and works out what the client's problem costs them and what solving it is worth, using only their own numbers. Every gap becomes a marked assumption with the question that confirms it. It then builds three options priced as a share of that value, each with a clear scope and what is not included, and prepares how to present them in under two minutes.

Log which option each client chose, and how each project turned out. It learns your real win rate per option and the share of value you actually win at.

## Who it is for

Freelancers, consultants, agencies and anyone who writes proposals for client projects.

## What you need

- Your discovery call notes or transcript, including any numbers the client mentioned.
- Your cost to deliver the work: your time, any subcontractors and tools.
- Your floor: the lowest price at which the work is worth doing for you.
- Any AI assistant. A paid plan is needed only to install it as a Claude skill.

## Three ways to use it

### 1. In any AI chat, with nothing installed

Open a new chat, attach `SKILL.md` and the three files in `Resources`, then paste this:

```text
Use the attached Value Pricing skill and its resources.
Price this project. Here are my discovery notes:
[paste them]
My cost to deliver the core work is [cost].
My floor is [floor].
```

The chat has no memory between runs, so it ends by printing a one-line proposal log. Keep it, and paste your log in next time so it can compare with past projects.

### 2. As a Claude skill

Custom skills need a paid Claude plan (Pro or above) with code execution switched on. These steps were checked against [Anthropic's help page](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) on 16 Nov 2026.

1. Download this `value-pricing` folder and compress it into a zip file. The folder itself must sit at the top of the zip.
2. In Claude, open **Customize**, then **Skills**. On some accounts this is under **Settings**, then **Capabilities**.
3. Click **+**, choose **Create skill**, then **Upload a skill**, and pick the zip file.
4. Start a new chat and type "price this project".

### 3. As a CoworkOS pack, with memory and learning

[CoworkOS](https://github.com/theAnirudhKumar/CoworkOS) is a folder of plain files that gives your AI a memory. Installed there, Value Pricing keeps your private floor, every proposal and its outcome, and your calibrated pricing shares, and reminds you to log each outcome.

Paste this into your CoworkOS assistant:

```text
Add the Value Pricing system to my CoworkOS. Get the
value-pricing folder from https://github.com/Hustlyst/Systems
and save it as a new area called Value Pricing, keeping its
files as they are. Do not change any of my existing files.
Then read its CLAUDE.md and tell me how to run it.
```

## A worked example

An online furniture shop whose checkout breaks on mobile phones.

- **From the notes:** about 30 abandoned mobile checkouts a week, at an average order of 380, by the client's own estimate.
- **Assumption:** a fix recovers 30 to 50 percent of those orders. To confirm, ask: "Of the people who abandon, how many come back and buy later?"
- **Value of solving it:** 30 orders × 380 × 52 weeks × 30 to 50 percent, which is about 178,000 to 296,000 a year. Pricing uses the low end.
- **Options:**
  1. Fix the checkout: 18,000.
  2. The fix plus abandoned-checkout recovery emails: 28,000.
  3. Both, plus three months of conversion testing: 38,000.
- **Floor (private):** 9,000.
- **For comparison:** hourly pricing would have quoted about 6,000 for the same core fix.

## What it never does

- It never treats a guess as a fact. Every number it did not get from the client is marked as an assumption.
- It never prices below your floor, and never shows the floor to the client.
- It never sends a proposal, email or invoice without your explicit yes.

## Files

| File | What it is |
| :-- | :-- |
| `SKILL.md` | Three runs: price a project, log an outcome, and calibrate |
| `Resources/rubric.md` | The three numbers, rules for assumptions, kinds of value, the three options, the floor and the checks before sending |
| `Resources/edge-cases.md` | No numbers, value that is hard to measure, fixed budgets, procurement rate cards, repeat clients, small projects, very large value, and retainers |
| `Resources/output-template.md` | The value case, the options, the price conversation and the outcome task |
| `CLAUDE.md` and `MEMORY.md` | The CoworkOS area. `MEMORY.md` starts empty |

Part of [Hustlyst Systems](../README.md). More practical AI for people who do not code at [hustlyst.com](https://hustlyst.com/?ref=github).
