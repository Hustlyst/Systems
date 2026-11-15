# Deal X-ray report template

Every run uses this shape, so this month's report can be laid next to last month's.

```text
DEAL X-RAY: [deal label] | [value] | stage [stage]
Close date in CRM: [date] | Pushed before: [number of times]
Run on: [date] | Previous run: [date, or "first run"]

VERDICT: [Commit / Best case / Pipeline]
Why, in one sentence: [reason]
Change since last run: [up / down / same, and why]

THE EIGHT POINTS
Point              Grade     Evidence
Metrics            [grade]   [quote and source, or what is assumed]
Economic buyer     [grade]   [...]
Decision criteria  [grade]   [...]
Decision process   [grade]   [...]
Paper process      [grade]   [...]
Identified pain    [grade]   [...]
Champion           [grade]   [influence / access / reason: each yes or no]
Competition        [grade]   [...]

THE GAP MOST LIKELY TO KILL IT
[point]: [one sentence on why, using the current weights]

ASK THIS ON THE NEXT CALL
"[the question, in words the seller would actually say]"

DATES TO THE SIGNATURE
Step                   Who            Realistic date
[step]                 [role]         [date]
Honest close date: [date]

TASKS
- [ ] [action] (due YYYY-MM-DD)
- [ ] [action] (due YYYY-MM-DD)

NOT JUDGED
[anything the material did not cover]
```

## Pipeline summary, when several deals are run together

```text
PIPELINE X-RAY: [date] | [number] deals | [total value]

Verdict     Deals   Value    Change since last run
Commit      [n]     [v]      [+/-]
Best case   [n]     [v]      [+/-]
Pipeline    [n]     [v]      [+/-]

Commit deals with the economic buyer missing: [list]
Deals pushed at least once: [n], [share of commit value]
Most common gap across all deals: [point]
```
