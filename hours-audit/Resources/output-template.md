# Hours Audit report templates

## The labelled rows, for pasting into a spreadsheet

The skill returns only this table, with one row per request and no totals.

```text
Request | Type | Repeat | Root cause | Confidence
1 | where is my reimbursement | yes | missing information | high
2 | invoice dispute | no | wrong form or tool | high
```

## The audit report

Written after the person pastes back the pivot table totals.

```text
HOURS AUDIT: [team] | [month] | [n] requests
Run on: [date] | Previous audit: [date, or "first audit"]

TOTAL HOURS ON REQUESTS: [hours] (last audit: [hours])
Share that were repeats: [share]%

TOP TEN BY HOURS
#  Type                 Requests  Minutes  Hours  Repeats  Main cause
1  [type]               [n]       [m]      [h]    [share]  [cause]
...

LAST AUDIT'S FIXES
Fix              Type         Result       Hours then  Hours now
[fix]            [type]       [result]     [h]         [h]

FIXES THIS MONTH, BY HOURS SAVED PER UNIT OF EFFORT
1. [type]: [fix] | kind: [kind] | effort: [size]
   Expected saving: [h] hours a month | Owner: [who]
2. ...

TASKS
- [ ] [fix] (due YYYY-MM-DD)

LOW-CONFIDENCE LABELS TO CHECK BY HAND: [n]
```
