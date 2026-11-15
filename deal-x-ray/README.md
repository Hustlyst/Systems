# Deal X-ray

Find out which of your deals are real before your forecast call, using only what your buyers actually said.

Deal X-ray reads your call notes and transcripts and checks each deal against MEDDPICC, the checklist experienced sales managers use. Every point is graded Proven by a buyer quote, Assumed, or Missing. You get the gap most likely to kill the deal, the exact question to ask on your next call, an honest close date and a list of dated tasks.

Each run is compared with the last one, so you see which deals are moving and which are stuck. Once you log a few wins and losses, it learns which gaps actually cost you deals and weights them more heavily.

## Who it is for

Account executives, founders who sell, and sales managers preparing a forecast or a pipeline review. It works for any deal with more than one call behind it.

## What you need

- Call transcripts or notes for each deal. Transcripts give the best result, because buyer quotes can only come from the buyer's own words.
- The deal value, stage and close date.
- Any AI assistant. A paid plan is needed only to install it as a Claude skill.

Remove customer names and confidential figures first, or describe them, unless your company allows them in AI tools.

## What MEDDPICC checks

| Point | The question behind it |
| :-- | :-- |
| Metrics | What measurable result does the buyer expect? |
| Economic buyer | Who can approve the money? |
| Decision criteria | What will they compare options on? |
| Decision process | What are the steps and dates between now and a yes? |
| Paper process | What do legal, security and procurement need? |
| Identified pain | What is the problem, in their words, and what does it cost them? |
| Champion | Who sells for you inside, with influence, access and a reason of their own? |
| Competition | What else could they do, including nothing? |

## Three ways to use it

### 1. In any AI chat, with nothing installed

Open a new chat, attach `SKILL.md` and the three files in `Resources`, then paste this:

```text
Use the attached Deal X-ray skill and its resources.
X-ray this deal. Here are my notes and transcripts:
[paste them, or attach them]
Value: [value]. Stage: [stage]. Close date: [date].
The close date has moved [number] times.
```

The chat has no memory between runs, so the report ends with a one-line run log. Keep it, and paste it in next time so the comparison still works.

### 2. As a Claude skill

Custom skills need a paid Claude plan (Pro or above) with code execution switched on. These steps were checked against [Anthropic's help page](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) on 16 Nov 2026.

1. Download this `deal-x-ray` folder and compress it into a zip file. The folder itself must sit at the top of the zip.
2. In Claude, open **Customize**, then **Skills**. On some accounts this is under **Settings**, then **Capabilities**.
3. Click **+**, choose **Create skill**, then **Upload a skill**, and pick the zip file.
4. Start a new chat and type "X-ray this deal".

### 3. As a CoworkOS pack, with memory and learning

[CoworkOS](https://github.com/theAnirudhKumar/CoworkOS) is a folder of plain files that gives your AI a memory. Installed there, Deal X-ray keeps every run, your deal outcomes and its own tuned weights, and its tasks appear in your daily brief.

Paste this into your CoworkOS assistant:

```text
Add the Deal X-ray system to my CoworkOS. Get the deal-x-ray
folder from https://github.com/Hustlyst/Systems and save it
as a new area called Deal X-ray, keeping its files as they
are. Do not change any of my existing files. Then read its
CLAUDE.md and tell me how to run it.
```

## A worked example

A 45,000 deal with a regional insurance firm, in commit for this month, with three call transcripts.

| Point | Grade | Why |
| :-- | :-- | :-- |
| Metrics | Assumed | The seller wrote "cut claim handling time". The buyer never gave a number. |
| Economic buyer | Missing | Every call was with the claims manager. Nobody has met the person who signs. |
| Decision criteria | Proven | The buyer sent a list of four requirements after call two. |
| Decision process | Assumed | The CRM says "final review". The buyer has not described the steps. |
| Paper process | Missing | Nobody has asked about security review. |
| Identified pain | Proven | "We lost two adjusters last quarter because the backlog burned them out." |
| Champion | Assumed | The claims manager is keen, but nothing shows access to the budget holder. |
| Competition | Missing | Nobody has asked what else they are considering. |

- **Verdict:** pipeline. With the economic buyer missing and no champion proven, this deal does not belong in commit.
- **The gap most likely to kill it:** the economic buyer, weight 3.
- **Ask on the next call:** "When you've made a decision like this before, who signed it off, and what did they need to see?"
- **Honest close date:** next quarter, once a security review of four to six weeks is allowed for.

## What it never does

- It never writes to your CRM, sends an email or books a meeting without your explicit yes.
- It never fills a gap with what is typical for an industry. A point with no evidence stays Missing.
- It never decides on discounts or terms.

## Files

| File | What it is |
| :-- | :-- |
| `SKILL.md` | The four runs: one deal, the whole pipeline, logging an outcome, and calibrating the weights |
| `Resources/rubric.md` | How each point is graded, the weights, what must be proven by each stage, and the verdict rules |
| `Resources/edge-cases.md` | Renewals, partners, small and large deals, notes only, quiet buyers, lost champions, early discount requests |
| `Resources/output-template.md` | The fixed report shape |
| `CLAUDE.md` and `MEMORY.md` | The CoworkOS area files. `MEMORY.md` starts empty |

Part of [Hustlyst Systems](../README.md). More practical AI for people who do not code at [hustlyst.com](https://hustlyst.com/?ref=github).
