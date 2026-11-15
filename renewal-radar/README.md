# Renewal Radar

See every renewal in your window on one page each month, ranked by what you could actually lose, with last month's view beside it.

Most renewal reviews rank accounts by a health colour. Renewal Radar ranks them by expected dollars lost and by the days left before the customer can give notice. It shows what moved since last month, which saves are stuck, and which accounts share one cause that only a product or pricing decision can fix. Every play becomes a dated task.

Once you log a few renewals, contractions and churns, it learns which warning signs actually came before losses in your own book, and checks those first.

## Built on CS Pulse's renewal-risk skill

The read on each single account comes from [`renewal-risk`](https://github.com/CSPulse/customer-success-skills/tree/main/skills/renewal-risk), part of CS Pulse's free customer success skills. That skill reads the signals that predict a renewal, from the person who signs down to usage patterns. It tags every piece of evidence as something said, seen or inferred, and gives a dollar range and one play.

Renewal Radar runs that read across the whole window and adds the monthly view, the comparison, the escalations and the learning. You need both.

## Who it is for

Customer success managers, account managers and their managers, with a book of renewing accounts.

## What you need

- A list of accounts with their annual value, renewal date, notice period and segment. A CRM export or a spreadsheet works.
- For each account in the window: recent call notes, emails, usage numbers and support tickets, whatever you have.
- The `renewal-risk` skill from CS Pulse.
- Any AI assistant. A paid plan is needed only to install it as a Claude skill.

Remove customer names and confidential figures first, or describe them, unless your company allows them in AI tools.

## Three ways to use it

### 1. In any AI chat, with nothing installed

Download this `renewal-radar` folder and CS Pulse's `renewal-risk` folder. Open a new chat, attach both `SKILL.md` files and their `Resources` and `references` files, then paste this:

```text
Use the attached Renewal Radar and renewal-risk skills.
Run my renewal radar. Here is my account list:
[paste or attach it]
And here is the material for each account:
[paste or attach notes, emails and usage]
```

The chat has no memory between runs, so the radar ends with a compact table. Keep it, and paste it in next month so the comparison still works.

### 2. As Claude skills

Custom skills need a paid Claude plan (Pro or above) with code execution switched on. These steps were checked against [Anthropic's help page](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) on 16 Nov 2026.

1. Download both the `renewal-radar` folder and CS Pulse's `renewal-risk` folder, and compress each into its own zip file. Each folder must sit at the top of its zip.
2. In Claude, open **Customize**, then **Skills**. On some accounts this is under **Settings**, then **Capabilities**.
3. Click **+**, choose **Create skill**, then **Upload a skill**. Upload one zip, then repeat for the other.
4. Start a new chat and type "run my renewal radar".

### 3. As a CoworkOS pack, with memory and learning

[CoworkOS](https://github.com/theAnirudhKumar/CoworkOS) is a folder of plain files that gives your AI a memory. Installed there, Renewal Radar keeps every month's radar, your renewal outcomes and the signals proven in your book, and its plays appear in your daily brief.

Paste this into your CoworkOS assistant:

```text
Add the Renewal Radar system to my CoworkOS. Get the
renewal-radar folder from https://github.com/Hustlyst/Systems
and save it as a new area called Renewal Radar, keeping its
files as they are. Also get the renewal-risk skill folder from
https://github.com/CSPulse/customer-success-skills and set it
up as a skill. Do not change any of my existing files. Then
read the Renewal Radar CLAUDE.md and tell me how to run it.
```

## A worked example

A book with 14 accounts in the window. Three of them:

| # | Account | Value | Call | Expected loss | Opt-out in | Person who signs met |
| --: | :-- | --: | :-- | --: | --: | :-- |
| 1 | Freight company | 180,000 | Contract | 45,000 | 58 days | No |
| 2 | Regional clinic group | 95,000 | Churn | 95,000 | 120 days | Yes |
| 3 | Marketing agency | 40,000 | Contract | 15,000 | 22 days | Yes |

- **Moved since last month:** the freight company dropped from renew to contract after a new finance lead arrived and their team asked for a seat usage export.
- **Ranking:** the marketing agency moves to the top despite its size, because it is inside 30 days of its opt-out date.
- **Shared risk:** the clinic group and two smaller accounts all cite the same missing integration. That goes to the manager as one product decision worth 160,000 in total.
- **Top play:** meet the freight company's new finance lead before the opt-out date, introduced by the existing contact, with the audit costs avoided in numbers.

## What it never does

- It never changes a CRM record, sends a message or books a meeting without your explicit yes.
- It never decides on a discount. It prepares you. The commercial decision stays with you and your company.
- It never guesses about an account it cannot read. That account goes on the "not checked" list with a task to start a conversation.

## Files

| File | What it is |
| :-- | :-- |
| `SKILL.md` | The four runs: the monthly radar, logging an outcome, calibrating, and preparing one save |
| `Resources/rubric.md` | The window by segment, ranking, what counts as a change, escalation levels, shared risks, and what calibration looks for |
| `Resources/edge-cases.md` | Multi-year contracts, consumption pricing, auto-renewals, accounts still being set up, a new book, a very large book, acquisitions, and accounts with little material |
| `Resources/output-template.md` | The fixed monthly radar |
| `CLAUDE.md` and `MEMORY.md` | The CoworkOS area. `MEMORY.md` starts empty |

Part of [Hustlyst Systems](../README.md). More practical AI for people who do not code at [hustlyst.com](https://hustlyst.com/?ref=github).
