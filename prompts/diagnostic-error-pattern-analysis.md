# Prompt: Cambridge Exam Diagnostic — Error Pattern Analysis

**Category:** AI-Assisted Exam Prep  
**Exam Target:** Cambridge B1 Preliminary (PET) — adaptable to other Cambridge exams  
**Use Case:** Cold test post-analysis · Root cause diagnosis · Study plan input  
**Last Updated:** 2026-04-02

---

## Purpose

This prompt helps distinguish between two fundamentally different failure types
in Cambridge reading and listening tests:

- **Strategy Collapse** — the student has the underlying ability but lacks the
  task framework (fixable in 1–2 weeks with targeted drilling)
- **Ability Gap** — the student genuinely lacks vocabulary, grammar, or
  listening stamina (requires sustained accumulation)

Misreading one as the other leads to wrong training prescriptions.

---

## The Prompt
```
You are an expert Cambridge exam coach analyzing a student's cold test results.

## Student Profile
- Name/alias: [e.g., Nova]
- Age: [e.g., 9]
- Native language: [e.g., Mandarin Chinese]
- Estimated level before test: [e.g., KET pass, working toward PET]

## Test Results
Provide scores per part, e.g.:

Reading:
- Part 1 (short notices matching): [X]/5
- Part 2 (multi-condition matching): [X]/5
- Part 3 (long text multiple choice): [X]/5
- Part 4 (gapped text): [X]/5
- Part 5 (vocabulary multiple choice): [X]/6
- Part 6 (open cloze): [X]/6
Total: [X]/32

Listening:
- Part 1 (picture selection): [X]/7
- Part 2 (short dialogue multiple choice): [X]/6
- Part 3 (form fill): [X]/6
- Part 4 (long interview multiple choice): [X]/6
Total: [X]/25

## Specific Error Notes
[Paste any observed patterns, e.g.:
- Q14 listening: heard the word correctly but misspelled it
- Part 4 reading: left 4 out of 5 blank
- Part 2 reading: matched on first keyword, stopped checking conditions]

## Your Analysis Task

1. **Score Summary**: State where the student sits relative to Grade C / B / A
   thresholds (C: ~140/170, B: ~153/170, A: ~160/170 on Cambridge scale).

2. **Error Pattern Classification**: For each underperforming part, classify as:
   - STRATEGY COLLAPSE (task framework missing)
   - ABILITY GAP (knowledge/skill deficit)
   - MIXED (both present)
   
   Explain your reasoning with reference to the specific errors observed.

3. **Shared Root Causes**: Identify if multiple parts share the same underlying
   failure mechanism (e.g., "passive linear processing" affecting both Reading
   Part 4 and Listening Part 3).

4. **Priority Repair Order**: List the top 2–3 interventions ranked by
   effort-to-score-gain ratio. Distinguish between:
   - Quick wins (1–2 weeks, strategy installation)
   - Medium-term gains (3–5 weeks, targeted practice)
   - Long-term accumulation (vocabulary, stamina)

5. **Red Flags**: Note any results that seem inconsistent with the student's
   profile (e.g., near-perfect score on a hard part alongside zero on an easier
   one) — these often indicate test anxiety, task misunderstanding, or an
   unrecognized strength.
```

---

## How to Use

1. Fill in the student profile and test results sections with actual data.
2. Add specific error notes — the more precise, the better the diagnosis.
   Photos of marked test papers can be described or attached as context.
3. Run in Claude (Sonnet or Opus recommended for nuanced pattern analysis).
4. Use the output to populate your error log and build a week-by-week study plan.

---

## Real-World Output Example

Applied to Nova's April 2026 cold test (PET Reading 19/32, Listening 15/25),
this prompt identified three cross-cutting error patterns:

| Pattern | Affected Parts | Fix Type |
|---------|---------------|----------|
| Strategy Collapse: no pre-scan framework | Reading P4 + Listening P3 | Strategy install, ~1 week |
| Surface matching → premature stop | Reading P2/P3 + Listening P2 | Drill with verification step |
| Short context > long context difficulty | Listening P2 vs P4 | Stamina + exposure |

Key insight: Listening Part 4 (100%) vs Part 3 (0%) in the same session confirmed
the issue was task-format unfamiliarity, not listening ability — a distinction
that completely changes the training prescription.

---

## Notes on Privacy

- Student names in this repo use aliases.
- No school names, test dates with identifying information, or personal data
  are included in prompt files.
- Raw test scores are included only as anonymized examples.

---

## Related Files

- `study-plans/` — 9-week PET prep framework (coming soon)
- `prompts/weekly-review-checklist.md` — (coming soon)
```




