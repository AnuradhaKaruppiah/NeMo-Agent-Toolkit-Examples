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

For each section, write enough that another engineer could understand your evaluation design after the interview. Use the guidelines as light prompts; skip anything that is not needed.

## 1. Evaluation Objective

What decision should the evaluation help the team make?

Guidelines:

- Decision the evaluation supports.
- Audience and what would make the result actionable.

## 2. Representative Work

What work should the agent be evaluated on? Include any data sources, task types, or benchmarks you would use.

Guidelines:

- Work or data included.
- Coverage gaps and release-gating relevance.

## 3. Success Criteria

How would you decide whether the agent solved the user's problem?

Guidelines:

- Success signals.
- Judgment method and scoring risks.

## 4. Evidence From A Run

What would you collect from each run before trusting the result?

Guidelines:

- Run artifacts to collect.
- How each artifact supports scoring, debugging, audit, or reproducibility.

## 5. Agent Configuration

What should be recorded about the agent version, available capabilities, environment, and constraints?

Guidelines:

- Agent, tool, environment, and constraint details to record.
- Which details affect fair comparison.

## 6. Path Quality

How would you judge whether the agent took an acceptable path to the result?

Guidelines:

- Process signals to inspect.
- Acceptable versus concerning path behavior.

## 7. Execution And Harness Strategy

Where should evaluation run, and what should be standardized across local, sandboxed, benchmark, or enterprise-like runs?

Guidelines:

- Execution modes to use.
- What must stay standardized and what risks remain.

## 8. Variant Comparison

How would you compare two agent versions fairly?

Guidelines:

- Comparison question and method.
- Evidence needed before trusting the result.

## 9. Failure Categories

How would you group failures so the team can act on them?

Guidelines:

- Failure categories.
- Example symptom and likely owner or fix path.

## 10. Scaling And Release Recommendation

What would make you ship, hold, or roll back a new version? How would this work daily, weekly, and at release time?

Guidelines:

- Daily, weekly, and release-time checks.
- Reviewers and ship, hold, or rollback criteria.

Final recommendation:

- Decision and key reason.

Open questions:

- Questions that could change the design or decision.
