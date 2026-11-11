# Results and Measurements

## 1. Start with the results page

### 1.1 Reading order

Check that the run has completed and identify the condition you are viewing. Results are not a single score: the process summary, agent states, Surveyor, Rater, and event logs answer different questions.

1. Read the process summary for major events and turning points.
2. Check agent states, need gaps, and logs.
3. Read Surveyor summaries and item-level answers for the relevant condition.
4. Review Rater hits, scores, and supporting evidence.
5. Use **View Logs** to verify unclear readings against steps, dialogue, and events.
6. Repeat the same reading order for other conditions before comparing.

Surveyor questionnaires are answered by the simulated AI agents. They are not surveys of real people and do not constitute a real participant sample.

### 1.2 Sections, conditions, and process summaries

The overall summary usually includes global steps, events, scenes, and the main interactions and transitions. In the example below, the baseline has 10 state steps, 10 log records, and three scenes. These counts describe the saved process; they are not Surveyor or Rater scores.

```{image} _static/screenshots/05-results-analysis.png
:alt: Results overview with 10 steps, 10 records, and three scenes
:width: 100%
:align: center
```

Condition buttons switch the summary and agent-state view. Surveyor and Rater instead group cards by condition within their own sections. The baseline has no added intervention; intervention conditions add a particular measure. Discuss differences only when comparable conditions are available.

Summaries do not replace step-by-step logs. If a summary differs from your expectation, check the logs for what agents actually did, when the intervention occurred, and which agents encountered it.

## 2. Agent states

Agent-state analysis uses states recorded throughout the simulation, rather than questionnaire answers or Rater scores. Select a condition, an agent, and a state metric such as need gap, SVO, own satisfaction, or satisfaction with others.

### 2.1 Select a condition, agent, and metric

Cards display goals, state characteristics, key changes, and metrics. State-step and action counts indicate the coverage of the current data.

```{image} _static/screenshots/09a-results-role-summary.png
:alt: Agent-state overview and selection controls
:width: 100%
:align: center
```

### 2.2 Curves and core needs

The horizontal axis uses global steps. Hover over a curve to read a step's value and corresponding action. Interpret changes through the full event log; a curve alone does not identify a cause.

```{image} _static/screenshots/09b-results-role-detail.png
:alt: Value-gap curve and core-need details
:width: 100%
:align: center
```

Core needs are recorded on a 0–10 scale:

| Field | Meaning |
| --- | --- |
| Initial value | State at the start of the simulation. |
| Final value | State at the end of the current condition. |
| Expected value | State the agent aims to reach. |
| Need gap | Expected value minus current value. |
| Change | Final gap minus initial gap. |

A positive gap means the current value is below the expected value; zero means it meets the expectation; a negative gap means it exceeds it. A negative change means the gap narrowed; a positive change means it widened. Total need gap sums the individual gaps. Inspect the details to locate specific changes.

The largest-gap indicator identifies the need furthest below its expected state at the end; largest change identifies the need with the greatest change in its gap. Satisfaction and SVO are simulated state indicators, not satisfaction-questionnaire responses.

## 3. Surveyor: questionnaires answered by simulated agents

Surveyor presents the configured questionnaire or psychological scale to the designated simulated AI agents, records their item-level answers, and calculates summaries according to that tool's implementation. Scenarios can use different tools and target agents; check the configuration currently shown.

### 3.1 Review the scale and summaries

Check the scale name, description, target agent, and condition before reading respondent counts, item counts, summary metrics, and measurement targets. Interpret score direction through the scale description; do not directly compare raw scores from different scales.

### 3.2 Expand records to check aggregation

Detailed records may include respondent-level totals and means for each dimension or component. These and the item-level answers are two views of the same measurement, not two separate surveys.

```{image} _static/screenshots/10d-results-surveyor-expanded-record.png
:alt: Expanded Surveyor aggregate records
:width: 100%
:align: center
```

Surveyor records come from simulated agents' questionnaire answers. A matching named behavior does not have to appear in the interaction log. Still consult the log to understand the simulated experience behind those answers.

### 3.3 Item-level answers and coding

Expand **Surveyor Answers** when available to inspect the item text, answer, saved numeric value, and dimension.

| Field | Meaning |
| --- | --- |
| Agent | Simulated agent answering the item. |
| ID | Item identifier used to match the same question. |
| Statement | Questionnaire item or statement. |
| Answer | Saved text answer from the simulated agent. |
| Value | Numeric answer code stored by the current tool implementation. |
| Dimension | Scale dimension, when provided. |

```{image} _static/screenshots/10e-results-surveyor-questionnaire-answers.png
:alt: Illustrative CAS item-level answers, values, and dimensions
:width: 100%
:align: center
```

**Value** is the numeric coding of an answer. In the illustrated CAS records, “Agree” is coded as 3, “Neither agree nor disagree” as 2, and “Strongly disagree” as 0. Check both **Answer** and the scale description: coding and aggregation differ between tools. Before comparing conditions, match the scale, target agent, and items.

## 4. Rater: behavioral analysis from logs

Rater checks whether the current condition's logs contain observable behaviors matching the scenario's rating criteria. It complements Surveyor: Surveyor records how simulated agents answer questionnaires; Rater identifies behavioral evidence in their interaction logs.

### 4.1 Run and view ratings

1. Expand **AI Rater (Behavior Analysis)**.
2. Select the agent to analyze.
3. Select one or more configured rating criteria.
4. Run the rating.
5. Review the generated cards under each condition.

```{image} _static/screenshots/11a-results-rater-baseline.png
:alt: Rater targets, tools, and rating controls
:width: 100%
:align: center
```

Rater reads the condition's full event log, checks behaviors against its criteria, and retains records supported by dialogue or event evidence. Some ratings are generated during simulation. After changing targets or criteria, you can rerun ratings on the results page.

### 4.2 Read cards and evidence

Available fields vary with the tool and saved records:

| Field | Interpretation |
| --- | --- |
| Detected behaviors | Number of evidence-supported hits under the selected criteria. |
| Mean score | Mean score for hit records, if provided. |
| Mean severity | Mean severity of detected behaviors, if provided. |
| Principal agents | Agents appearing most often in the detected records, if provided. |
| Representative evidence | Summarized evidence extracted from the logs, if provided. |
| Detailed records | Steps, scenes, agents, categories, scores, or evidence for detected behaviors, as available. |

No detected behavior means no clear matching evidence was found in the current logs, not proof that the behavior cannot exist. Compare hits, scores, and severity only under the same criteria. Inspect available record-level evidence and full logs before drawing conclusions.

## 5. Compare conditions

### 5.1 Use a consistent reading order

Match agents, state metrics, scales, respondents, and rating criteria across baseline and intervention conditions.

| Layer | What to compare | How to verify |
| --- | --- | --- |
| Interaction process | Main events and turning points. | Check when the intervention occurred and how agents responded. |
| Agent states | Need gaps, satisfaction, and SVO. | Locate corresponding global steps and actions. |
| Surveyor | Aggregates for the same scale and agent. | Check item-level Answer, Value, and coding. |
| Rater | Hits and available summary metrics. | Inspect detailed evidence and full logs. |

Use logs to check timing, exposure to the intervention, subsequent actions, and whether those actions correspond to state or measurement changes. Logs, states, Surveyor, and Rater have different data sources; none substitutes for all the others.

For example, if an agent's final need gap is 4 in the baseline and 1 in the intervention condition, that means the agent ended closer to its expected state in this simulation. Also check matching Surveyor records, available Rater evidence, and logs. A difference in one run does not establish a general causal effect.

Different scales can have different ranges, directions, and coding. Do not compare their raw values directly. Retain experimental conditions, agent settings, available measurement records, and original interaction logs with your results.

## 6. Common questions

| Situation | What to check |
| --- | --- |
| No Surveyor or Rater results | Check run completion, configured tools, the relevant condition group, and page messages. The scenario may not have the corresponding tool. |
| Only a baseline is available | Add and enable a custom intervention, then run the combined comparison. Older interfaces may provide separate intervention or all-condition modes. |
| Questionnaire values exist without matching behavioral evidence | This can occur: Surveyor records simulated questionnaire answers, while Rater uses log evidence and rating criteria. |
| Real-model and simulated-test labels | These identify the measurement execution mode. Check that it fits your purpose; test-mode results should not be treated as formal findings. A real-model label does not mean the participants are real people. |
| Older results lack charts, summaries, or fields | Check existing logs and measurement records first. Rerun if you need the complete current result structure. |
