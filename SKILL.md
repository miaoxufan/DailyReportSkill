---
name: research-weekly-report
description: Create and maintain concise research weekly reports from experiment logs, metric tables, notes, and workspace records. Use when the user asks for a weekly report, experiment progress summary, research milestone update, or a structured record of completed work, failures, conclusions, and next steps.
---

# Research Weekly Report

## Purpose

Produce an evidence-based weekly report for an ongoing research project. Preserve the difference between completed results, current progress, interpretation, and proposed work. Prefer updating an existing report in the user's workspace when one exists.

## Workflow

1. Locate the project workspace and existing weekly/report records.
2. Collect only relevant evidence: experiment logs, validation summaries, figures, code changes, and dated notes.
3. Build a chronological experiment table with dataset, model, training setting, status, and formal metrics.
4. Separate formal validation metrics from provisional training metrics, visual observations, and hypotheses.
5. Summarize what changed, what was learned, what failed, and why it matters to the research question.
6. State unresolved risks and the next experiment with a concrete acceptance criterion.
7. Write or update the report, preserving prior entries and adding the report date.
8. Link local evidence files when possible. Do not invent missing metrics or present an unverified result as final.

## Report structure

Use this order unless the user requests another format:

1. Reporting period and project focus
2. Executive summary (2–5 sentences)
3. Completed experiments
4. Formal results table
5. Interpretation and research significance
6. Failures, limitations, and data-quality issues
7. Decisions made
8. Next-week experiments and success criteria
9. Evidence links

## Metric discipline

- Label metrics as `formal`, `online/provisional`, `visual`, or `planned`.
- Prefer dedicated full-volume validation outputs over patch-level training logs.
- Report the evaluation split, number of validation cases, label aggregation, and whether background or near-zero labels were excluded.
- Keep baseline and proposed methods comparable: same split, preprocessing, checkpoint selection, and inference protocol.
- When a result is negative or inconclusive, state that directly.

## Research writing style

- Use concise technical Chinese by default unless the user requests English.
- Describe the causal claim conservatively: distinguish “supports,” “suggests,” and “demonstrates.”
- Do not hide preprocessing, data cleaning, or selection rules. If data are private, describe the procedure at an appropriate high level.
- Make the next action operational: specify dataset, method, epoch budget, output metric, and stopping rule.

## Output modes

- For a quick update, return a compact Markdown report in the conversation.
- For a persistent record, write Markdown in the project's `experiments/` or `reports/` directory.
- For a formal Word report, use the `documents` skill after assembling and checking the content.
- For a presentation-style weekly review, use the `ppt-skill` after the report content is stable.

## Evidence checklist

Before finalizing, verify:

- every reported number has a source file or log;
- current experiments are clearly marked as running;
- failed experiments are not counted as results;
- best and final checkpoints are distinguished;
- next steps follow from the evidence rather than optimism.
