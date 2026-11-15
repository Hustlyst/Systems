---
name: deal-x-ray
description: >
  Deal X-ray, deal review, forecast prep, MEDDPICC check, is this deal real, X-ray my pipeline, log a deal outcome, calibrate my deal X-ray. Checks a sales deal against MEDDPICC using the seller's own call notes and transcripts. Grades every point as Proven by a buyer quote, Assumed or Missing, names the gap most likely to kill the deal using weights learned from the seller's own wins and losses, writes the exact question for the next call, works out an honest close date, and turns each action into a dated task. Compares every run with the last one. Use before a forecast call, a pipeline review or a deal handover.
---

# Deal X Ray

Check a deal the way a strict sales manager does before a forecast, using only what the buyer actually said. Each run is compared with the last one, and the weights behind "the gap most likely to kill it" are tuned from the seller's own won and lost deals.

## Before you start

1. Read `Resources/rubric.md`, `Resources/edge-cases.md` and `Resources/output-template.md`.
2. Read `MEMORY.md` if it exists. Take the current weights from it, and find the last run for this deal, if there is one. If there is no `MEMORY.md`, use the starting weights in the rubric and say this is a first run.
3. Remind the seller once: remove anything their company does not allow in an AI tool, such as customer names or contract values, or describe them instead. Do not ask again on later runs.

## Run 1: X-ray one deal

**Trigger:** "X-ray this deal", "deal review", "is this deal real".

### Step 1. Collect the material

Ask for, in this order of value:

1. Call transcripts, or the recording tool's export.
2. Emails and documents the buyer sent.
3. The seller's own notes.
4. The deal value, stage, close date in the CRM, and how many times the close date has moved.

If a connected tool holds any of this, such as a meeting recorder, email or the CRM, offer to read it. Read only. Never write to the CRM or send anything.

If only notes are available, follow the "only the seller's notes" case in `edge-cases.md`.

### Step 2. Grade the eight points

For each point in the rubric:

- Give a grade: Proven, Assumed or Missing.
- For Proven, quote the buyer's words and say where they come from.
- For Assumed, say what is assumed and who said it.
- For the champion, mark influence, access and a personal reason separately as yes or no.

Apply the rubric strictly. A buyer agreeing with the seller's summary is Assumed.

### Step 3. Check against the stage

Compare the grades with the table "What must be proven by each stage" in the rubric. List every point that should be Proven for the claimed stage but is not.

### Step 4. Find the gap most likely to kill it

Among the points that are not Proven, take the one with the highest current weight. Inside 30 days of the close date, the paper process weight rises to 4. Ties go to the economic buyer, then the champion.

Explain in one sentence why this gap matters for this deal, using the deal's own facts.

### Step 5. Write the question for the next call

Write one question that would close that gap if the buyer answers it honestly. Write it the way the seller would say it out loud: short, open, with no jargon and no mention of MEDDPICC. Examples:

- Economic buyer: "When you've made a decision like this before, who signed it off, and what did they need to see?"
- Paper process: "Once your team says yes, what happens next on your side: legal, security, procurement? How long does each usually take?"
- Champion: "If this goes ahead, what changes for you personally?"

### Step 6. Work out an honest close date

List every step from today to a signature, using only what the buyer has described. Put a realistic date on each, and use the buyer's own estimates where they gave one. If the steps do not fit before the CRM close date, give the honest date.

### Step 7. Give the verdict

Use the verdict rules in the rubric, including the rule about deals pushed before.

### Step 8. Compare with the last run

If `MEMORY.md` has an earlier run for this deal, show what changed: grades that moved, the verdict, and whether the question from last time was asked and answered. If the same gap has stayed open across two runs, say so plainly. It is the clearest sign a deal is stuck.

### Step 9. Turn actions into tasks

Write each action as a task in this form, with a real date:

```text
- [ ] Ask Priya's team who signs above 30,000 (due 2026-11-21)
```

In CoworkOS, add the tasks to the Next Actions section of this area's `MEMORY.md`, so they appear in the daily brief. Elsewhere, list them at the end of the report.

### Step 10. Record the run

Write the report in the shape set by `output-template.md`.

Then add one line to the run log in `MEMORY.md`. This skill owns that log and may write to it without asking. Everything else in `MEMORY.md` still needs the person's yes.

If there is no `MEMORY.md`, for example in a plain chat, print the run-log line at the end and tell the person to keep it. They paste it back next time so the comparison still works.

## Run 2: X-ray the pipeline

**Trigger:** "X-ray my pipeline", "forecast prep".

1. Run Run 1 for each deal the seller plans to commit or call best case. Keep each report short: the verdict, the gap and the question.
2. Then produce the pipeline summary from `output-template.md`.
3. Flag every commit deal with the economic buyer Missing, and every deal pushed more than once.
4. End with the three questions that would move the most value if they were answered this week.

## Run 3: Log an outcome

**Trigger:** "log a deal outcome", "we won", "we lost", "the deal slipped".

1. Ask for the deal, the result (won, lost or slipped) and the reason in the buyer's own words, if the seller has them.
2. Find the last X-ray of that deal in `MEMORY.md` and copy its eight grades into the outcomes table.
3. Ask for a yes before saving the outcome, then save it.

Remind the person at the weekly review to log any deal that closed that week. Outcomes are what make the weights accurate.

## Run 4: Calibrate the weights

**Trigger:** "calibrate my deal X-ray", or once a quarter during the weekly review.

This needs at least 8 closed deals with an X-ray before close, including at least 3 lost. With fewer, say how many more are needed and stop.

1. For each of the eight points, count:
   - In lost deals, how often the point was Missing or Assumed at the last X-ray.
   - In won deals, how often the same was true.
2. Work out the difference between the two shares, as percentage points.
3. Propose changes:
   - A difference of 30 points or more: raise the weight by 1.
   - A difference of zero or below: lower the weight by 1.
   - Anything in between: leave it.
   - Keep every weight between 1 and 4.
4. Show the table of counts, differences and proposed weights, with one sentence on what it means for this seller.
5. Change the weights in `MEMORY.md` only after the person says yes, and note the date of the change.

These counts are small, so treat them as a guide. Never change a weight on fewer deals than the minimum above.

## Rules that always apply

- Use only what is in the material. If a point is not covered, it is Missing. Never fill a gap with what is typical for the industry.
- Quote the buyer word for word. Never tidy a quote.
- Read only from connected tools. Never update the CRM, send an email or book anything without the person's explicit yes.
- Be direct about the verdict. If a deal should come out of commit, say so in the first line.
- The X-ray prepares the seller. It never decides on discounts or terms.
