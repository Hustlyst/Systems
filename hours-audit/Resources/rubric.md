# Hours Audit rubric

This file sets how requests are labelled, how hours are counted, and how fixes are chosen and judged. The skill reads it on every run, so one month's audit can be compared with the next.

## The one rule that makes the numbers trustworthy

**The AI labels. The spreadsheet counts.**

AI is good at reading a request and deciding what kind it is. It is unreliable at counting hundreds of rows, and it will give a confident total that is wrong. So the AI never adds anything up. It returns one labelled row per request, and a spreadsheet pivot table does every count and every total.

## The request types

Types are agreed with the team on the first run, from a sample of about 50 requests, and then kept stable so months can be compared. A good list has:

- Between 8 and 12 types.
- A one-line definition and two example requests for each.
- Names in the team's own words, for example "where is my reimbursement" rather than "finance query".
- One type called "other", which should hold less than a tenth of requests. If it holds more, the list is missing a type.

Change the list only between audits, and record the change in `MEMORY.md`, so a jump in one type is never just a renamed type.

## What each row gets

| Field | Values | How it is decided |
| :-- | :-- | :-- |
| Type | One from the agreed list | From the request text |
| Repeat | Yes or no | Yes when the same question has been answered before, for this person or someone else |
| Root cause | One from the list below | From what the request reveals |
| Confidence | High or low | Low when the request is too short or vague to label |

### Root causes

| Root cause | What it means | Example |
| :-- | :-- | :-- |
| Missing information | The answer exists but people cannot find it | "Where's the travel policy?" |
| Wrong form or tool | The form asks for the wrong thing, so people come back | "I submitted it but it needs a cost centre" |
| Broken handoff | Work stalls between two teams | "Sales closed it, who sets up the account?" |
| Unclear decision rights | Nobody knows who may decide | "Can I approve this discount?" |
| Genuine one-off | A real exception | "Our office flooded" |

## Minutes per type

The team gives a typical handling time per type, in minutes, including the back-and-forth. When people disagree, use the middle value and note the range. These estimates drive every total, so check the top three types with the people who handle them.

## Choosing fixes

Each of the ten types with the most hours gets one fix, from this list, in this order of preference:

1. **Remove the need.** Change the process so the request never happens.
2. **Let people help themselves.** Make the answer findable: a status column, a short guide, a pinned answer.
3. **Use a template.** Pre-write the reply or the form.
4. **Automate it.** A rule or a tool does the step.
5. **Move it.** Hand it to someone better placed.

Effort is small (under a day), medium (under two weeks) or large. Rank fixes by **hours saved per month divided by effort**, where small is 1, medium is 3 and large is 8.

## Judging a fix

On the next audit, each fix from last time is checked against its type.

| Result | Rule |
| :-- | :-- |
| **Worked** | The type's hours fell by at least half the expected saving |
| **Partly worked** | They fell, but by less than half the expected saving |
| **Did not work** | They did not fall, or they rose |
| **Not done** | The fix was never made |

A fix that did not work usually means the root cause was wrong. The next audit looks at those requests again before suggesting a new fix.

## What the learning step looks for

Over several audits, the skill counts which kinds of fix worked in this team, for example "self-serve fixes worked 4 times out of 5, automation 1 time out of 3". It then prefers the kinds that work here when suggesting fixes, and says why.
