# Research-agent instructions

This repository contains PhD research based on menstrual-cycle data. Read the project README and the study's analysis plan, variable definitions, and data documentation before reviewing or changing any analysis.

Follow the shared [AI-assisted research review protocol](https://github.com/dvirross/research-agents/pull/7). Assess the research question, target population, measurement definitions, design, and limits before auditing supplementary methods or code. Trace every reported result to its source data, analysis, and output; distinguish confirmed findings from hypotheses and prioritize by effect on the study's conclusions.

## Health-data privacy

- Treat participant-level health data as sensitive. Do not send row-level records, direct identifiers, re-identification keys, or sensitive combinations of variables to any model API or external service without explicit authorization.
- Prefer local analysis and appropriately aggregated, disclosure-safe summaries. Do not include participant data in commits, issues, pull requests, logs, or agent prompts.
- Preserve raw source data and provenance. Add analysis in separate files unless the project owner explicitly directs otherwise.

## Statistical review

Check the operational definitions, inclusion and exclusion rules, repeated measurements within participants, missingness, selection, time ordering, uncertainty, and multiplicity where relevant. Separate descriptive results from inferential claims and avoid causal language unless the design supports it. Verify model-proposed findings against the data and code; the model's own attribution is not independent confirmation. Request extra analyses only when they address a named uncertainty that could change an interpretation.

## AI-assisted change attribution

Record AI use in the final Git commit so later reviews can identify which tools and model versions contributed to each change. Add these Git trailers at the end of every commit containing AI-assisted work:

```
AI-Assisted: yes
AI-Use: <tool or interface> | <exact model name and version> | <role and scope of contribution>
```

Repeat `AI-Use` once for each model that contributed. Use the model name and version shown in the interface or API; do not infer it or use a generic label such as “Claude” or “GPT” by itself. If the model identifier was not exposed, write `unknown (not exposed)` and do not claim greater precision. Describe the contribution narrowly (for example: literature search, proof exploration, statistical analysis, coding, testing, drafting, editing, translation, or review) so the record does not imply that a model did the entire change. For a commit with no AI assistance, use `AI-Assisted: no`.

Preserve these trailers when commits are squashed or rebased. Do not put prompts, private session URLs, unpublished sensitive data, personal data, or credentials in commit metadata.

For manuscripts and research reports, prepare any AI-use disclosure from these records and the project’s usage notes, then follow the target journal’s disclosure rules. State the exact tool and model versions and the actual contribution where requested; distinguish research or analysis assistance from coding, writing, editing, translation, and review. Do not infer use that the records do not support. Human authors remain responsible for checking claims, citations, calculations, and the final text.

Research-specific rule: preserve enough non-sensitive scope in each `AI-Use` trailer to support a later publication disclosure (for example, which analysis, proof, literature task, or manuscript section). Record whether the output was independently checked when that affects interpretation. Never include participant-level data or confidential source material in attribution metadata.
