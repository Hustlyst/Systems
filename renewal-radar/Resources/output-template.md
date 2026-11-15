# Renewal Radar report template

Every run uses this shape, so this month's radar can be laid next to last month's.

```text
RENEWAL RADAR: [month] | [number] accounts in the window
Run on: [date] | Previous run: [date, or "first run"]

TOTALS
Annual value in the window:   [total]
Expected renewal value:       [total]
Expected loss:                [total], down / up [amount] since last month

RANKED BY EXPECTED LOSS
#  Account         Value   Call       Expected loss  Opt-out in  Decider met
1  [account]       [v]     [call]     [loss]         [days]      [yes/no]
2  ...

MOVED SINCE LAST MONTH
- [account]: [old call] to [new call], because [new evidence]

STUCK
- [account]: play "[play]" passed its checkpoint on [date]

SHARED RISKS
- [mechanism]: [accounts], [total dollars]. Needs a product or
  pricing decision, owner: manager

TOP THREE PLAYS THIS MONTH
1. [account]: [play] | Owner: [who] | By: [date]
   Checkpoint: "If [thing] has not happened by [date], [escalation]."
2. ...
3. ...

ESCALATIONS
Level 2: [accounts]
Level 3: [accounts]

SIGNALS PROVEN IN YOUR BOOK
- [signal]: present before [n] of your last [n] losses

TASKS
- [ ] [action] (due YYYY-MM-DD)

NOT CHECKED
- [accounts with too little material for a read]
```

The single-account reads behind the table follow the `renewal-risk` output format. Keep them in a separate section or file, so the radar itself fits on one page.
