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

For each section, write enough that another engineer could understand your evaluation design after the interview.

## 1. Evaluation Objective

What decision should the evaluation help the team make?

| Field | Candidate Notes |
|-------|-----------------|
| Primary decision | |
| Secondary decisions | |
| Who uses the result? | |
| What would make the evaluation actionable? | |

## 2. Representative Work

What work should the agent be evaluated on? Include any data sources, task types, or benchmarks you would use.

| Source or task type | Why include it? | What can it miss? | Ready for release gate? |
|---------------------|-----------------|-------------------|--------------------------|
| | | | |
| | | | |
| | | | |

## 3. Success Criteria

How would you decide whether the agent solved the user's problem?

| Signal | Automatic, human, or hybrid? | Strengths | Failure modes |
|--------|------------------------------|-----------|---------------|
| | | | |
| | | | |
| | | | |

## 4. Evidence From A Run

What would you collect from each run before trusting the result?

| Evidence | Why collect it? | Used for scoring, debugging, or audit? |
|----------|-----------------|----------------------------------------|
| | | |
| | | |
| | | |
| | | |

## 5. Agent Configuration

What should be recorded about the agent version, available capabilities, environment, and constraints?

| Configuration item | Why it matters | How it affects comparison |
|--------------------|----------------|---------------------------|
| | | |
| | | |
| | | |
| | | |

## 6. Path Quality

How would you judge whether the agent took an acceptable path to the result?

| Process signal | Good behavior | Concerning behavior | How to measure or review |
|----------------|---------------|---------------------|--------------------------|
| | | | |
| | | | |
| | | | |

## 7. Execution And Harness Strategy

Where should evaluation run, and what should be standardized across local, sandboxed, benchmark, or enterprise-like runs?

| Execution mode | Purpose | What should be standardized? | Main risk |
|----------------|---------|------------------------------|-----------|
| | | | |
| | | | |
| | | | |

## 8. Variant Comparison

How would you compare two agent versions fairly?

| Comparison question | Proposed method | Minimum evidence before trusting it |
|---------------------|-----------------|------------------------------------|
| | | |
| | | |
| | | |

## 9. Failure Categories

How would you group failures so the team can act on them?

| Failure category | Example symptom | Likely owner or fix path |
|------------------|-----------------|--------------------------|
| | | |
| | | |
| | | |
| | | |

## 10. Scaling And Release Recommendation

What would make you ship, hold, or roll back a new version? How would this work daily, weekly, and at release time?

| Cadence | What runs? | Who reviews? | Ship or hold criteria |
|---------|------------|--------------|-----------------------|
| Daily | | | |
| Weekly | | | |
| Release | | | |

Final recommendation:

-

Open questions:

-
