# Renewal Radar rubric

This file sets how the Radar chooses accounts, ranks them and decides when to escalate. The read on each single account comes from the `renewal-risk` skill by CS Pulse, which carries the signal tiers and the evidence tags. This file never restates that method. It decides what to do with many reads at once.

## Which accounts are in the window

An account enters the Radar when its **opt-out date**, not its renewal date, falls inside the window for its segment. The opt-out date is the renewal date minus the notice period in the contract.

| Segment | Start reading this many months before the opt-out date |
| :-- | :-- |
| Enterprise | 9 to 12 |
| Mid-market | 6 |
| Small business | 1 to 2 |

These follow the timing in `renewal-risk`'s context adjustments. Change them in `MEMORY.md` if your own book shows decisions being made earlier or later.

An account with no known notice period uses its renewal date, and the Radar adds a task to find the notice period.

## How accounts are ranked

Each account's `renewal-risk` read gives a dollar range and an expected renewal value. The Radar works out two numbers.

1. **Expected loss:** the current annual value minus the expected renewal value. A full churn expected loss is the whole contract. A likely contraction is the size of the expected cut.
2. **Days to opt-out:** the days left before the customer can give notice.

Accounts are ranked by expected loss, highest first. Two adjustments then apply:

- An account inside 30 days of its opt-out date moves to the top, whatever its value. After that date most of the options are gone.
- An account where nobody can name the person who signs moves up one place for every month it stays unnamed. The rule in `renewal-risk` is that no decider means no green call.

## What counts as a change since last month

The Radar compares every account with its last read in `MEMORY.md`.

| Change | What it means | What the Radar does |
| :-- | :-- | :-- |
| The call moved down, for example from renew to contract | A new signal arrived | Shows the new evidence first |
| The expected loss grew by more than a fifth | The risk got bigger | Lists it in "Moved since last month" |
| The same play is still open after its checkpoint date | The save is stuck | Escalates it by one level |
| The decider is still unnamed for a second month | The account is flying blind | Escalates it by one level |
| The call moved up | A play worked, or a signal faded | Records which play, for the learning step |

## When to escalate

| Level | Who acts | When |
| :-- | :-- | :-- |
| 1. The CSM alone | The account owner | Every account in the window with a call of contract or churn |
| 2. With the manager | The CSM and their manager | Expected loss above the threshold in `MEMORY.md`, or a stuck play |
| 3. With an executive | An executive sponsor on our side | Inside 60 days of opt-out with a churn call, or the decider unmet at level 2 for a month |

The money threshold for level 2 starts at the median contract value in the book. Set your own in `MEMORY.md`.

## Risks that share one cause

When three or more accounts carry the same mechanism, such as the same missing feature, the same price increase or the same competitor, the Radar groups them as one risk. One product or pricing decision fixes all of them, and no single CSM can. It goes to the manager as a group, with the total dollars.

## What the learning step looks for

After every logged outcome, the Radar notes which signals were present at the last read before the result. Once a quarter, with enough outcomes, it compares:

- Signals present before a churn or contraction.
- Signals present before a full renewal.

A signal that appeared before most of your losses and rarely before your renewals is marked **proven in your book**. The Radar checks those signals first and names them in the report. A signal that appeared just as often before renewals is marked **noise in your book**, and the Radar stops giving it prominence for that segment.

This never overrides the `renewal-risk` rules, such as "no decider, no green". It changes which evidence the Radar looks for first and puts first in the report.
