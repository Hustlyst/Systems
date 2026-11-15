# Customer Language

Write your marketing in the words your customers already use, with every line traced back to real customers.

Customer Language collects the exact words people use in your sales calls, reviews, support tickets and surveys. It sorts them into six groups: the moment they started looking, the pain, the result they wanted, what nearly stopped them, the words they use for the problem, and what else they tried. It counts which ideas come up again and again across separate sources. Then it scores your current copy line by line, and rewrites it so the headline uses a phrase at least three customers used.

The bank grows every quarter. Log your copy tests, and it learns which kind of message wins with your audience, for example whether leading with the pain beats leading with the result.

## Who it is for

Marketers, founders who write their own copy, and anyone writing a homepage, ads, emails or sales slides.

## What you need

- At least 30 pieces of raw customer language, from more than one kind of source. Sales call transcripts, your reviews and your competitors' reviews, survey answers and support tickets all work.
- The copy you want to audit or rewrite.
- Any AI assistant. A paid plan is needed only to install it as a Claude skill.

Remove names and personal details from the sources first.

## Three ways to use it

### 1. In any AI chat, with nothing installed

Open a new chat, attach `SKILL.md` and the three files in `Resources`, then paste this:

```text
Use the attached Customer Language skill and its resources.
Build a language bank from these sources:
[paste or attach them, about ten at a time]
Then audit this copy and rewrite it:
[paste the copy]
```

The chat has no memory between runs, so it ends by printing the bank. Keep it, and attach it next time.

### 2. As a Claude skill

Custom skills need a paid Claude plan (Pro or above) with code execution switched on. These steps were checked against [Anthropic's help page](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) on 16 Nov 2026.

1. Download this `customer-language` folder and compress it into a zip file. The folder itself must sit at the top of the zip.
2. In Claude, open **Customize**, then **Skills**. On some accounts this is under **Settings**, then **Capabilities**.
3. Click **+**, choose **Create skill**, then **Upload a skill**, and pick the zip file.
4. Start a new chat and type "build a language bank".

### 3. As a CoworkOS pack, with memory and learning

[CoworkOS](https://github.com/theAnirudhKumar/CoworkOS) is a folder of plain files that gives your AI a memory. Installed there, Customer Language keeps your bank for each kind of buyer, your copy scores over time and your test history, and reminds you to log each test result.

Paste this into your CoworkOS assistant:

```text
Add the Customer Language system to my CoworkOS. Get the
customer-language folder from https://github.com/Hustlyst/Systems
and save it as a new area called Customer Language, keeping
its files as they are. Do not change any of my existing files.
Then read its CLAUDE.md and tell me how to run it.
```

## A worked example

A scheduling tool for clinics, with 40 sources: 12 sales calls, 20 reviews and 8 cancellation survey answers.

- **Trigger, 9 sources from calls and reviews:** "We lost two patients in one week because of double bookings."
- **Words:** customers say "front desk" and "no-shows". The website says "patient engagement platform", a phrase no customer used.
- **Copy score before:** 2 of 9 homepage lines backed, 22%.
- **Old headline:** "The all-in-one patient engagement platform."
- **New headline:** "Stop double bookings and no-shows before they cost your front desk another patient." It is backed by quotes from 9, 7 and 5 sources.
- **Test plan:** old against new headline on the pricing page for four weeks. Success means more demo requests per visitor.

## Its companion for product teams

[CS Pulse's voice-of-customer skill](https://github.com/CSPulse/customer-success-skills/tree/main/skills/voice-of-customer) turns the same kind of material into a product feedback report, with themes ranked by the revenue behind them. Customer Language uses customers' words for marketing. That skill uses them to decide what to build.

## What it never does

- It never paraphrases a quote. Customers' exact words are the point.
- It never publishes a customer's quote as a testimonial. That needs their permission.
- It never publishes, sends or changes anything without your explicit yes.

## Files

| File | What it is |
| :-- | :-- |
| `SKILL.md` | Five runs: build the bank, audit copy, rewrite, log a test, and learn what wins |
| `Resources/rubric.md` | The six groups, which sources count most, what makes a pattern, how copy is scored, and the rewriting rules |
| `Resources/edge-cases.md` | Few sources, a new product, several kinds of buyer, long B2B cycles, rewarded reviews, other languages, regulated industries, and conflicts with positioning |
| `Resources/output-template.md` | The bank update, the copy audit, the rewrite and the test log |
| `CLAUDE.md` and `MEMORY.md` | The CoworkOS area. `MEMORY.md` starts empty |

Part of [Hustlyst Systems](../README.md). More practical AI for people who do not code at [hustlyst.com](https://hustlyst.com/?ref=github).
