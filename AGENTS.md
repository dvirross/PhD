# Research-agent instructions

This repository contains PhD research based on menstrual-cycle data. Read the project README and the study's analysis plan, variable definitions, and data documentation before reviewing or changing any analysis.

Follow the shared [AI-assisted research review protocol](https://github.com/dvirross/research-agents/pull/7). Assess the research question, target population, measurement definitions, design, and limits before auditing supplementary methods or code. Trace every reported result to its source data, analysis, and output; distinguish confirmed findings from hypotheses and prioritize by effect on the study's conclusions.

## Health-data privacy

- Treat participant-level health data as sensitive. Do not send row-level records, direct identifiers, re-identification keys, or sensitive combinations of variables to any model API or external service without explicit authorization.
- Prefer local analysis and appropriately aggregated, disclosure-safe summaries. Do not include participant data in commits, issues, pull requests, logs, or agent prompts.
- Preserve raw source data and provenance. Add analysis in separate files unless the project owner explicitly directs otherwise.

## Statistical review

Check the operational definitions, inclusion and exclusion rules, repeated measurements within participants, missingness, selection, time ordering, uncertainty, and multiplicity where relevant. Separate descriptive results from inferential claims and avoid causal language unless the design supports it. Verify model-proposed findings against the data and code; the model's own attribution is not independent confirmation. Request extra analyses only when they address a named uncertainty that could change an interpretation.
