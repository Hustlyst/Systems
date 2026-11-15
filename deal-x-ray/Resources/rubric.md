# Deal X-ray rubric

This file is the scoring standard. The skill reads it on every run, so two people looking at the same deal reach the same answer.

## How each point is graded

Every point gets one of three grades.

| Grade | What it means | What counts as evidence |
| :-- | :-- | :-- |
| **Proven** | The buyer said it or did it. | A line the buyer said or wrote, quoted with where it came from: a call date, an email or a document they sent. An action they took also counts, such as sending a security questionnaire. |
| **Assumed** | We believe it, but the buyer has not confirmed it. | Something the seller said, wrote in notes or summarised, and the buyer only nodded along. Anything inferred from the company's size, industry or job titles. |
| **Missing** | Nothing in the material covers it. | No evidence either way. |

**A buyer agreeing with the seller's summary is Assumed.** "Yes, that sounds right" confirms that the buyer heard the seller. It does not prove the point.

## The eight points

Each point has a starting weight from 1 to 4. The weights decide which gap is "most likely to kill the deal". They are adjusted by the calibration step in `SKILL.md` once there are enough closed deals, and the current weights are kept in `MEMORY.md`.

### 1. Metrics, starting weight 2

**Definition:** the measurable result the buyer expects, in their numbers.

- **Strong evidence:** the buyer names a number and a time frame. Example: "We need to get claim handling from nine days to five before the renewal season."
- **Weak evidence:** a direction with no number, such as "we want to be faster".
- **Why it matters:** with no number, there is no business case to take to the person who signs, and the deal competes on price.

### 2. Economic buyer, starting weight 3

**Definition:** the person who can approve the money, and who can say yes when others say no.

- **Strong evidence:** the seller has met them, or the buyer has named them and described what they need to see. Example: "Priya signs anything over 30,000, and she wants a payback under a year."
- **Weak evidence:** a job title guessed from the org chart.
- **Why it matters:** deals with no access to the economic buyer stall at the end, when the budget question finally reaches someone who was never part of the decision.

### 3. Decision criteria, starting weight 1

**Definition:** what the buyer will compare the options on.

- **Strong evidence:** a written list, a scorecard or an RFP, or the buyer naming their top three criteria.
- **Weak evidence:** features the seller demonstrated that the buyer liked.

### 4. Decision process, starting weight 2

**Definition:** the steps and the people between now and a yes, in order, with dates.

- **Strong evidence:** the buyer has described the steps. Example: "Team review next week, then it goes to the leadership meeting on the 14th."
- **Weak evidence:** the stages in the seller's own CRM.

### 5. Paper process, starting weight 2, rising to 4 inside 30 days of close

**Definition:** the legal, security, procurement and signature steps.

- **Strong evidence:** the buyer has named the steps and how long each usually takes, or one has already started.
- **Weak evidence:** "legal should be fine".
- **Why the weight rises:** paper work is the most common reason a deal that everyone agreed to still slips past quarter end.

### 6. Identified pain, starting weight 2

**Definition:** the problem in the buyer's words, with a cost attached.

- **Strong evidence:** the buyer describes the problem and what it costs them, in time, money or risk.
- **Weak evidence:** a pain the seller suggested and the buyer agreed with.

### 7. Champion, starting weight 3

**Definition:** someone inside the buyer's company who sells for you when you are not in the room.

A contact only counts as a **proven** champion when the material shows all three of these:

1. **Influence:** others act on what they say.
2. **Access:** they can reach the economic buyer.
3. **A personal reason:** they gain something themselves if this goes ahead.

Someone who likes the seller but has none of the three is a friendly contact, graded Assumed.

### 8. Competition, starting weight 1

**Definition:** every other option the buyer has, including doing nothing, building it themselves, or spending the budget elsewhere.

- **Strong evidence:** the buyer has named the alternatives and how they compare.
- **Weak evidence:** "they did not mention anyone else". Silence about competition is graded Missing. It does not mean there is none.

## What must be proven by each stage

A deal can be early and still healthy. The question is whether the right points are proven for the stage it claims to be in.

| Stage | Points that should be Proven | Points that can still be Assumed |
| :-- | :-- | :-- |
| Discovery | Identified pain | Everything else |
| Evaluation | Pain, champion, decision criteria | Metrics, economic buyer, paper process |
| Proposal | Pain, champion, criteria, metrics, economic buyer | Paper process |
| Commit | All eight, with dates on the decision and paper process | None |

## The verdict

| Verdict | Rule |
| :-- | :-- |
| **Commit** | All eight points Proven, and every remaining step has a date that falls before the close date. |
| **Best case** | Pain, champion and economic buyer Proven, and the gaps can realistically close before the close date. |
| **Pipeline** | Any of pain, champion or economic buyer is Missing, or the close date is not honest. |

**One extra rule:** a deal whose close date has already been pushed once is no better than best case until the buyer gives a new date themselves.

## Healthy ranges for a team

These help when the skill reviews the whole pipeline. They are starting points, and the calibration step replaces them with the reader's own numbers.

- A deal in commit with the economic buyer Missing is the single biggest forecast risk. Treat any commit deal like that as best case.
- Treat it as a warning when more than a third of the commit value has already been pushed once. Check that share every month and let your own results show where the line should be.
