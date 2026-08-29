# Personal Learning Upgrade System — Agent Protocol

## Purpose

Maintain a long-running, evidence-based learning profile for the user. The
user's north-star objective is to research how dimensions and/or spacetime may
emerge. This repository is the durable record and scoring engine for that
journey, not an application.

## Source of truth

- `learning-profile.md` contains the current scores, evidence, and next actions.
- `daily-log.md` is append-only and records user reports and score changes.
- `assessment.md` contains the baseline assessment and calibration rubric.
- Git history is the audit trail. Never rewrite it without explicit permission.

## Scoring model

- Score each competency from 0–100, using the level bands in `assessment.md`.
- Do not award points merely for elapsed time. Award points for demonstrated
  work: problems solved, derivations reconstructed, active recall, projects,
  writing, exams, conversation, or verified output.
- Daily changes are normally +0.1 to +1.5 per relevant competency. Larger
  changes require a meaningful assessment result or durable artifact.
- Track confidence separately: `low`, `medium`, or `high`. A self-report alone
  starts at low confidence; tested performance raises it.
- Assign one study item to a primary competency and, where justified, one or
  two secondary competencies. Avoid double-counting.
- Record uncertainty, assumptions, and all score deltas in `daily-log.md`.

## Daily check-in workflow

When the user reports learning:

1. Extract topic, activity, time, difficulty, outcome, and evidence.
2. Map it to competencies in `learning-profile.md`.
3. Update the competency scores, evidence, and next action.
4. Append a dated audit entry to `daily-log.md`.
5. Commit the changed files with a concise, dated message if Git is available.
6. Report the score changes and one high-leverage next step in concise Chinese.

If the report lacks time or outcome, make a conservative provisional update and
ask only for the missing information that would materially change the score.

## Assessment workflow

- Run short diagnostic probes before treating a score as well-calibrated.
- Prefer adaptable questions: one concise theoretical prompt and one problem or
  application prompt for each subject.
- Never fabricate test answers or claim an uncompleted assessment was measured.
- Revise a baseline only when new evidence warrants it, keeping the prior value
  in the daily log.

## Scope and maintenance

- Preserve user data and unrelated working-tree changes.
- Keep files readable in Markdown and do not build an app unless explicitly
  requested.
- Commit local system changes. Pushing to a remote requires a configured remote
  and authenticated access; report any missing prerequisite clearly.
