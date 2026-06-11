<!--
SPDX-FileCopyrightText: Copyright (c) 2026, NVIDIA CORPORATION & AFFILIATES. All rights reserved.
SPDX-License-Identifier: Apache-2.0

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

# Candidate Live Worksheet

Use this worksheet during the interview as your working artifact. It is fine to leave sections incomplete; focus on decisions, assumptions, tradeoffs, and what evidence would change your mind.

For each section, write enough that another engineer could understand your evaluation design after the interview. Use the guidelines as prompts; you do not need to answer every bullet mechanically.

## 1. Evaluation Objective

What decision should the evaluation help the team make?

Guidelines:

- State the primary decision the evaluation should support, such as ship, block, compare variants, diagnose quality, or tune behavior.
- Note any secondary decisions the same evaluation could inform without stretching it beyond its purpose.
- Identify who will use the result and what level of detail they need.
- Explain what would make the result actionable, including thresholds, review expectations, or follow-up steps.

## 2. Representative Work

What work should the agent be evaluated on? Include any data sources, task types, or benchmarks you would use.

Guidelines:

- Choose tasks, datasets, or benchmarks that represent the agent's expected production workload.
- Explain why each source or task type belongs in the evaluation.
- Call out what each source can miss, such as long-tail behavior, rare tools, noisy inputs, or enterprise constraints.
- Distinguish release-gating work from exploratory or diagnostic work.

## 3. Success Criteria

How would you decide whether the agent solved the user's problem?

Guidelines:

- Define success signals that are grounded in the user's intended outcome, not only surface-level output quality.
- Decide which signals can be measured automatically, which require human judgment, and where a hybrid review is useful.
- Describe why each signal is trustworthy enough to influence the decision.
- Identify common failure modes, including false positives, false negatives, brittle scoring, and reviewer inconsistency.

## 4. Evidence From A Run

What would you collect from each run before trusting the result?

Guidelines:

- List the run artifacts needed to understand the result, such as inputs, outputs, traces, tool calls, logs, intermediate state, or environment details.
- Explain why each artifact is necessary before trusting the score or judgment.
- Separate evidence used for scoring from evidence used for debugging or audit.
- Note any privacy, retention, or reproducibility constraints that affect what can be collected.

## 5. Agent Configuration

What should be recorded about the agent version, available capabilities, environment, and constraints?

Guidelines:

- Record the agent version, model, prompts, tools, retrieval sources, memory behavior, policies, and runtime settings that could affect behavior.
- Include environment details that influence reproducibility, such as sandbox permissions, network access, credentials, timeouts, or available files.
- Explain why each configuration detail matters for interpreting the result.
- Identify which configuration changes would make two runs difficult to compare fairly.

## 6. Path Quality

How would you judge whether the agent took an acceptable path to the result?

Guidelines:

- Define process signals that matter beyond the final answer, such as planning, tool use, verification, safety checks, recovery, or user communication.
- Describe what good behavior looks like for the agent's path through the task.
- Describe concerning behavior, including avoidable risk, wasted steps, unsupported assumptions, hidden failures, or brittle retries.
- Decide how each process signal should be measured, reviewed, or sampled.

## 7. Execution And Harness Strategy

Where should evaluation run, and what should be standardized across local, sandboxed, benchmark, or enterprise-like runs?

Guidelines:

- Choose execution modes that match the evaluation purpose, such as local smoke tests, sandboxed regression tests, benchmark runs, or enterprise-like staging.
- State what must be standardized across runs, including data, prompts, tool availability, policies, seeds, timeouts, and scoring rules.
- Identify which differences between execution modes are intentional and which would bias the result.
- Call out the main operational risks, such as flakiness, data leakage, unavailable services, or unrealistic constraints.

## 8. Variant Comparison

How would you compare two agent versions fairly?

Guidelines:

- State the comparison question clearly, such as quality improvement, regression risk, cost, latency, reliability, or safety.
- Propose a method that controls for task mix, environment, scorer behavior, and randomness.
- Define the minimum evidence needed before trusting the comparison.
- Include how you would handle ties, mixed results, and differences that are statistically or practically small.

## 9. Failure Categories

How would you group failures so the team can act on them?

Guidelines:

- Group failures by likely fix path, not only by visible symptom.
- Include example symptoms that make each category recognizable during review.
- Identify the likely owner or next step for each category, such as prompt changes, tool reliability, data quality, model capability, policy, or product design.
- Keep categories specific enough to drive action but broad enough to track trends over time.

## 10. Scaling And Release Recommendation

What would make you ship, hold, or roll back a new version? How would this work daily, weekly, and at release time?

Guidelines:

- Describe what should run daily, weekly, and at release time.
- Identify who reviews each cadence and what level of evidence they need.
- Define ship, hold, and rollback criteria for the release decision.
- Include how the process should scale as tasks, agent capabilities, and stakeholders grow.

Final recommendation:

- Summarize whether you would ship, hold, or roll back, and name the strongest evidence behind that recommendation.

Open questions:

- List unresolved questions that would materially change the evaluation design or release decision.
