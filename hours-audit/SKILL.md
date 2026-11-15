---
name: hours-audit
description: >
  Hours audit, where do our hours go, what should we automate, audit our requests, label these tickets, which requests take the most time, check if our fixes worked. Finds the request types eating the most team hours from a month of help desk, shared inbox, form or chat requests. The AI labels each request with a type, a repeat flag and a root cause, and a spreadsheet does all the counting, because AI labels text well and counts it badly. Ranks the top ten types by hours, proposes one fix each ranked by hours saved per unit of effort, and on the next audit checks whether each fix actually saved the hours. Learns which kinds of fix work in this team. Use monthly or quarterly, and before any automation project.
---

# Hours Audit

Find where your team's hours really go, fix the biggest drains first, and check next month whether the fixes worked.

## Before you start

1. Read `Resources/rubric.md`, `Resources/edge-cases.md` and `Resources/output-template.md`.
2. Read `MEMORY.md` if it exists: the agreed request types, the minutes per type, last audit's totals and fixes, and what kinds of fix work in this team. With no `MEMORY.md`, say this is a first audit.
3. Remind the person once to remove personal or sensitive requests, as `edge-cases.md` describes.

## Run 1: The audit

**Trigger:** "run an hours audit", "where do our hours go", "what should we automate".

### Step 1. Get the export

Ask for one month of requests as a spreadsheet, one row per request with at least the text and the date, from every channel available. Offer to read a connected help desk or inbox. Read only. Number the rows if they are not already.

### Step 2. Agree the types (first audit only)

With no agreed list in `MEMORY.md`:

1. Read about 50 requests spread across the month.
2. Propose 8 to 12 types, each with a one-line definition and two examples, named in the team's own words.
3. Ask the person to edit the list until it matches how the team thinks about the work.
4. Ask for the typical minutes per type, including back-and-forth.
5. Save the list and the minutes to `MEMORY.md` after the person says yes.

On later audits, reuse the saved list. If the person wants to change it, record the change and the date.

### Step 3. Label every request

Label the requests in batches of about 100, using the rubric's fields: type, repeat, root cause and confidence.

**Return only the labelled table, in the format in `output-template.md`. Never count, add up or summarise.** If the person asks for a total, give the pivot table steps instead.

### Step 4. The person counts in a spreadsheet

Give these steps:

1. Paste the labelled rows next to the original export.
2. Add a column with the minutes for each row's type.
3. Insert a pivot table with Type as rows, and show the count of requests, the sum of minutes, and the count of repeats.
4. Divide the sum of minutes by 60 for hours.
5. Paste the pivot table back here.

### Step 5. Check a sample

Pick 20 random rows and ask the person to check the labels. If more than two are wrong, tighten the type definitions and relabel the batches with the most errors. Also list the low-confidence rows for a quick look.

### Step 6. Judge last audit's fixes

If `MEMORY.md` has fixes from last time, compare each one's type with its hours now, using the rubric's "Judging a fix" table. For any fix that did not work, look again at a sample of that type's requests before suggesting anything new. The root cause was probably wrong.

### Step 7. Propose fixes

For the ten types with the most hours, propose one fix each, from the rubric's list. Prefer the kinds of fix that `MEMORY.md` shows work in this team. Name who does the work after the fix, so work is removed rather than moved. Rank the fixes by hours saved per month divided by effort.

### Step 8. Tasks and the report

Turn each fix with an owner into a task with a real date:

```text
- [ ] Add a status column to the expenses sheet (due 2026-11-28)
```

In CoworkOS, add them to Next Actions in this area's `MEMORY.md`. Write the report in the shape set by `output-template.md`.

### Step 9. Save

Save this audit's totals per type and the fixes, with their expected savings, to `MEMORY.md`. This skill owns the audit history and may write it without asking. Other changes need a yes.

Without a `MEMORY.md`, print the totals and fixes at the end and ask the person to keep them for the next audit.

## Run 2: Learn which fixes work

**Trigger:** "which fixes work for us", or once a quarter.

This needs at least six judged fixes. With fewer, say how many more are needed and stop.

1. Count, for each kind of fix, how many worked, partly worked, did not work or were not done.
2. Report it in one plain sentence per kind, with the counts.
3. Point out any kind of fix that is often left undone. That usually means the effort was underestimated or nobody owned it.
4. Save the finding after the person says yes.

## Rules that always apply

- The AI labels. The spreadsheet counts. Never state a total the spreadsheet did not produce.
- Read only from connected tools. Never close a ticket, reply to anyone or change a system without an explicit yes.
- Count a fix as working only when total hours fall, not when work moves to another team.
- Leave out personal and sensitive requests unless the company allows them in AI tools.
