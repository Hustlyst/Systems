# Hustlyst Systems

Deep AI systems for people who do not code. Each one runs on your own material, such as call transcripts, account notes or customer reviews. It carries the method an experienced practitioner would use, checks its own output, and gets better every month as it learns from your results.

They are made for people in sales, marketing, customer success, operations, and freelance and consulting work.

## What makes a System different from a prompt

| A prompt | A System |
| :-- | :-- |
| Starts from nothing every time | Reads your own material |
| Gives everyone the same answer | Applies a written method with a scoring rubric |
| Forgets the last run | Compares each run with the last one |
| Stays the same | Learns from your wins and losses and tunes its weights |
| Ends with advice | Ends with dated tasks |

## The Systems

| System | For | What it does |
| :-- | :-- | :-- |
| [Deal X-ray](deal-x-ray/) | Sales | Checks each deal against MEDDPICC using what the buyer actually said, names the gap most likely to kill it, and gives the question for your next call |
| [Renewal Radar](renewal-radar/) | Customer success | Ranks every renewal in the window by expected dollars lost and days to opt-out, compares with last month and learns which signals came before your losses. Built on CS Pulse's renewal-risk skill |

## Three ways to use each one

1. **In any AI chat:** attach the System's files and paste the starter prompt from its page. Nothing to install.
2. **As a Claude skill:** upload the folder as a custom skill. This needs a paid Claude plan.
3. **As a CoworkOS pack:** drop it into [CoworkOS](https://github.com/theAnirudhKumar/CoworkOS), the plain-file second brain. This is the full version, with memory between runs, learning from outcomes, and tasks in your daily brief.

Each System's own page has the exact steps.

## What every System includes

| File | What it is |
| :-- | :-- |
| `README.md` | What it does, who it is for, how to install it and a worked example |
| `SKILL.md` | The runs themselves, in the Agent Skills format |
| `CLAUDE.md` | The area's rules, for CoworkOS |
| `MEMORY.md` | An empty template that fills in with every run |
| `Resources/` | The rubric, the report template and the edge cases |

## Privacy

Every System reads only. None of them sends a message, changes a record in a connected tool or books anything without your explicit yes. Remove customer names and confidential figures before you start, unless your company allows them in AI tools.

## Contributing

Spotted a mistake, or a case a System handles badly? Open an issue and describe the situation. Please never include real customer data in an issue.

## Licence

MIT. See [LICENSE](LICENSE).

---

Made by [Hustlyst](https://hustlyst.com/?ref=github): practical AI for people who do not code.
