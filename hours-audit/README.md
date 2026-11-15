# Hours Audit

Find out which requests are really eating your team's hours, fix the biggest drains first, and check next month whether the fixes worked.

Teams usually automate whatever is most annoying. The real cost tends to sit in small, frequent requests nobody notices, such as the same question asked 40 times a month. Hours Audit labels every request in a month's export with its type, whether it is a repeat, and its root cause. Your spreadsheet then counts the hours. It ranks the top ten drains, proposes one fix each, ordered by hours saved for the effort, and turns them into dated tasks.

On the next audit it checks each fix against the numbers. Over time it learns which kinds of fix actually work in your team.

## Why the spreadsheet does the counting

AI is good at reading a request and deciding what kind it is. It is unreliable at counting hundreds of rows, and it will give a confident total that is wrong. So Hours Audit only labels, and a pivot table in your spreadsheet does every count. That split is what makes the numbers worth acting on.

## Who it is for

Operations leads, team leads and anyone running a shared inbox, help desk or request queue.

## What you need

- One month of requests exported as a spreadsheet, with the request text and the date. A help desk, shared inbox, request form or chat channel export all work.
- A spreadsheet tool with pivot tables, such as Google Sheets or Excel.
- A rough idea from the team of how long each kind of request takes.
- Any AI assistant. A paid plan is needed only to install it as a Claude skill.

Remove personal or sensitive requests first, unless your company allows them in AI tools.

## Three ways to use it

### 1. In any AI chat, with nothing installed

Open a new chat, attach `SKILL.md` and the three files in `Resources`, then paste this:

```text
Use the attached Hours Audit skill and its resources.
Run an hours audit on this month of requests:
[attach the export]
```

The chat has no memory between runs, so it ends by printing your types, totals and fixes. Keep them, and attach them next month.

### 2. As a Claude skill

Custom skills need a paid Claude plan (Pro or above) with code execution switched on. These steps were checked against [Anthropic's help page](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) on 16 Nov 2026.

1. Download this `hours-audit` folder and compress it into a zip file. The folder itself must sit at the top of the zip.
2. In Claude, open **Customize**, then **Skills**. On some accounts this is under **Settings**, then **Capabilities**.
3. Click **+**, choose **Create skill**, then **Upload a skill**, and pick the zip file.
4. Start a new chat and type "run an hours audit".

### 3. As a CoworkOS pack, with memory and learning

[CoworkOS](https://github.com/theAnirudhKumar/CoworkOS) is a folder of plain files that gives your AI a memory. Installed there, Hours Audit keeps your agreed request types, every month's totals and every fix with its result, and the fixes appear in your daily brief.

Paste this into your CoworkOS assistant:

```text
Add the Hours Audit system to my CoworkOS. Get the
hours-audit folder from https://github.com/Hustlyst/Systems
and save it as a new area called Hours Audit, keeping its
files as they are. Do not change any of my existing files.
Then read its CLAUDE.md and tell me how to run it.
```

## A worked example

A 12-person finance operations team, with 1,140 requests in one month.

- **The biggest drain was not the one everyone complained about.** Invoice disputes felt worst. The top type by hours was "where is my reimbursement": 310 requests at about 6 minutes each, which is 31 hours a month.
- **270 of those 310 were repeats.**
- **Root cause:** missing information. Reimbursement status was only visible to the finance team.
- **Fix:** a status column in the shared expenses sheet. Kind: let people help themselves. Effort: small. Expected saving: about 25 hours a month.
- **Next audit:** the type fell to 9 hours, so the fix is marked as worked.

## What it never does

- It never reports a total the spreadsheet did not produce.
- It never closes a ticket, replies to anyone or changes a system without your explicit yes.
- It never counts a fix as working when the work has only moved to another team.

## Files

| File | What it is |
| :-- | :-- |
| `SKILL.md` | Two runs: the audit, and learning which fixes work |
| `Resources/rubric.md` | The labelling rule, request types, root causes, choosing fixes, judging them, and what the learning step looks for |
| `Resources/edge-cases.md` | Several channels, unusual months, vague or sensitive requests, very large exports, disagreement on minutes, fixes that move work, and fixes with no owner |
| `Resources/output-template.md` | The labelled rows and the audit report |
| `CLAUDE.md` and `MEMORY.md` | The CoworkOS area. `MEMORY.md` starts empty |

Part of [Hustlyst Systems](../README.md). More practical AI for people who do not code at [hustlyst.com](https://hustlyst.com/?ref=github).
