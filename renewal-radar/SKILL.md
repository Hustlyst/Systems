---
name: renewal-radar
description: >
  Renewal radar, run my renewal radar, renewal review, which renewals are at risk, churn review, portfolio risk, log a renewal outcome, calibrate my renewal radar. Runs the CS Pulse renewal-risk read across every account whose opt-out date falls in the window, ranks them by expected dollars lost and days to opt-out, compares with last month, groups accounts that share one cause, escalates stuck saves, and turns the top plays into dated tasks. Learns from logged renewals, contractions and churns which signals came before losses in this book. Needs the renewal-risk skill from github.com/CSPulse/customer-success-skills. Use monthly, and before a renewal forecast or a QBR with a manager.
---

# Renewal Radar

A monthly view of every renewal in the window, ranked by what is really at stake, with last month's view beside it. The read on each account comes from the `renewal-risk` skill by CS Pulse. This skill turns many reads into one plan.

## Before you start

1. Check that the `renewal-risk` skill is available. If it is not, stop and give the person this line, then wait:

   ```text
   Renewal Radar needs the renewal-risk skill. Get it from
   https://github.com/CSPulse/customer-success-skills
   (folder skills/renewal-risk), then ask me again.
   ```

2. Read `Resources/rubric.md`, `Resources/edge-cases.md` and `Resources/output-template.md`.
3. Read `MEMORY.md` if it exists: the window settings, the money threshold, last month's radar, open plays with their checkpoints, and the signals marked proven or noise in this book. With no `MEMORY.md`, say this is a first run.
4. Remind the person once to remove anything their company does not allow in an AI tool, or to describe it instead.

## Run 1: The monthly radar

**Trigger:** "run my renewal radar", "renewal review", "which renewals are at risk".

### Step 1. Build the list

Ask for the list of accounts with: current annual value, renewal date, notice period, segment, and the owner. A CRM export or a spreadsheet is ideal. If a connected tool holds this, offer to read it. Read only.

Work out each opt-out date, then keep the accounts whose opt-out date falls in the window for their segment. Add any multi-year account due its yearly read. Follow `edge-cases.md` for consumption pricing and auto-renewals.

### Step 2. Gather the material for each account

For each account in the window, collect what exists: recent call notes and transcripts, emails, usage exports, support tickets and the contract terms. Offer to read connected tools. With more than about 40 accounts, follow the "very large book" case.

### Step 3. Read each account

Run `renewal-risk` on each account and keep its full read. Put the signals marked "proven in your book" in `MEMORY.md` at the front of the evidence to look for.

Accounts with too little material go to "Not checked", with a task to get a conversation this month.

### Step 4. Rank and compare

1. Work out the expected loss and the days to opt-out for each account, as the rubric sets out.
2. Rank them, and apply the two adjustments in the rubric.
3. Compare with last month's radar in `MEMORY.md`, using the change table in the rubric. List what moved and what is stuck.
4. Group any three or more accounts that share one mechanism into a single shared risk.

### Step 5. Decide escalations

Apply the escalation levels in the rubric. Name the accounts at each level.

### Step 6. Choose the top three plays

Take the three plays that protect the most expected loss, starting with any account inside 30 days of opt-out. Each play keeps its owner, date and a checkpoint that can fail, as `renewal-risk` writes them.

### Step 7. Turn plays into tasks

Write each action as a task with a real date:

```text
- [ ] Meet the freight account's new finance lead (due 2026-12-05)
```

In CoworkOS, add them to Next Actions in this area's `MEMORY.md`, so they show in the daily brief. Elsewhere, list them at the end.

### Step 8. Save the radar

Write the radar in the shape set by `output-template.md`. Then save this month's ranked table and each play's checkpoint to `MEMORY.md`. This skill owns the radar history and may write it without asking. Every other change to `MEMORY.md` needs the person's yes.

Without a `MEMORY.md`, print a compact copy of the table at the end and ask the person to keep it for next month.

## Run 2: Log an outcome

**Trigger:** "log a renewal outcome", "they renewed", "they churned", "they cut seats".

1. Ask for the account, the result (full renewal, contraction with the size of the cut, or churn) and the reason in the customer's words, if known.
2. Find the last read of that account in `MEMORY.md`, and copy the signals present at that read.
3. Note which play was running and whether its checkpoint was met.
4. Save it after the person says yes.

At the weekly review, ask which renewals closed that week.

## Run 3: Calibrate

**Trigger:** "calibrate my renewal radar", or once a quarter during the weekly review.

This needs at least 10 logged outcomes, including at least 3 churns or contractions. With fewer, say how many more are needed and stop.

1. For each signal that appears in the logged reads, count how often it was present before a loss or a contraction, and how often before a full renewal.
2. Mark a signal **proven in your book** when it was present before at least half of the losses and before no more than a fifth of the renewals.
3. Mark it **noise in your book** when it was present before renewals at least as often as before losses.
4. Do this per segment when there are enough outcomes in each. Otherwise do it for the whole book and say so.
5. Show the table with one sentence on what it means. Save the marks only after the person says yes.
6. Also check which plays were followed by a renewal more often than not, and list them as the plays that work in this book.

## Run 4: Prepare one save

**Trigger:** "prepare the save for [account]".

Take that account's read and play. Write the opening three sentences for the conversation, starting from the customer's goals in their own words, naming what has been seen, and asking one open question. Then list what to bring: the value delivered with numbers, and what the person needs from their own company.

## Rules that always apply

- The single-account method belongs to `renewal-risk`. Follow its rules, including "no decider, no green" and "most at-risk accounts renew smaller, not never".
- Read only from connected tools. Never change a CRM record, send a message or book a meeting without an explicit yes.
- Never decide on a discount. The Radar prepares the person. Commercial decisions stay with them and their company.
- When an account cannot be read, say so. Never fill a gap with what is typical.
