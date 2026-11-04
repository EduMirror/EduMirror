# Platform Features

EduMirror organizes a simulation into six steps: Select Scenario, Modify Scenario, Configure Agents, Run Simulation, Results Analysis, and Media Generation. Revisit completed steps to review or edit settings.

```{image} _static/screenshots/00-steps.png
:alt: Six-step navigation
:width: 100%
:align: center
```

## Workflow and navigation

1. **Select Scenario**: open a built-in scenario or create one in the AI Scenario Workshop.
2. **Modify Scenario**: check scenes, interaction requirements, and agents' known information; add a custom intervention if needed.
3. **Configure Agents**: inspect agents by scene and adjust their runtime settings in the editor.
4. **Run Simulation**: run the baseline, optionally with a saved custom intervention, and follow live logs.
5. **Results Analysis**: review the process, agent needs, Surveyor questionnaires, and Rater behavioral scores.
6. **Media Generation**: generate comics, video prompts, and videos from the selected results.

The top step bar returns to completed steps. **View Logs** on the results page returns to the run step. The restart control clears the current workflow after confirmation and returns to scenario selection.

## 1. Select Scenario

```{image} _static/screenshots/01-select-scenario.png
:alt: Scenario selection page
:width: 100%
:align: center
```

The page contains scenario cards, a search box, and pagination. Enter a name or keyword to filter the list, or move between pages. Selecting a built-in scenario marks it as selected and opens **Modify Scenario**.

### Custom scenarios

Select **Custom Scenario** to open the **AI Scenario Workshop**. Describe a situation and AI will generate editable agents, scenes, conditions, and measurement settings.

#### Describe your request

In **What would you like to study?**, describe the participants, situation, behavior you want to observe, and whether you want an intervention. Everyday language is sufficient; names and detailed agent settings can be adjusted later.

For example:

> Simulate a student, a parent, and a teacher discussing AI use in homework under unclear assignment rules. Explore learning, fairness, and disclosure without forcing agreement. Use English throughout. All characters are fictional.

If you use news or other materials, provide a summary and source, and explain which details are simulation assumptions.

```{image} _static/screenshots/08-custom-scenario-workshop.png
:alt: AI Scenario Workshop request input and Send button
:width: 100%
:align: center
```

Click **Send**. AI organizes the research question, participants, context, and outcomes. Select the displayed answers or enter details, then submit your response. Once enough information is available, the platform generates the editable scenario canvas.

If the brief does not reflect your intention, describe the changes you need. If a fictional setting triggers a request for a report, clarify that it does not refer to a specific real event and answer any displayed follow-up question.

#### Review and edit the canvas

The canvas has three parts:

- **Context & roles**: edit the name, summary, scene sequence, and agent settings. Expand scenes to review their background, participants, known information, action requirements, and order; expand agents to inspect their identity and goals.
- **Interventions**: select the study design and review baseline and intervention conditions.
- **Outcome analysis**: configure research questions, hypotheses, questionnaires, behavioral ratings, and target agents. These are analysis settings; actual results become available after a run.

Edit individual fields directly. To coordinate changes across several fields, enter a request below the canvas and click **Send a revision**. Review the regenerated configuration for unintended changes elsewhere.

```{image} _static/screenshots/custom-generated-canvas.png
:alt: Editable canvas and the revision input below it
:width: 80%
:align: center
```

Use **Confirm and continue** to move between canvas sections. **Use this scenario** saves the configuration and opens the subsequent editor.

#### Choose the study design

The workshop may ask whether you want to **Observe only** or **Compare interventions**. Select an answer and click **Submit answers**. In the generated canvas, open **Interventions** to review or change **Study design**:

- **Observe naturally**: observe the baseline discussion.
- **Compare interventions**: review the baseline and intervention conditions.
- **Needs confirmation**: leave the choice open while refining the scenario.

```{image} _static/screenshots/custom-intervention-choice.png
:alt: Study-design dropdown, baseline, and intervention condition
:width: 100%
```

Expand each condition to check its details. Use **Confirm and continue** to proceed to outcome settings. You can save the scenario now and design additional interventions later in the separate workshop under **Modify Scenario**.

#### Save and continue editing

After checking the canvas, click **Use this scenario**. The workshop closes and **Modify Scenario** opens, with the source identified as a custom scenario.

Saving does not preserve the current AI conversation as an editable chat session. Use **Modify Scenario** for action requirements and known information, and **Configure Agents** for agent settings. To add another intervention, use the intervention workshop described below.

Saved custom scenarios appear on the workshop's left side. **Open** loads one into the editor. Starting another AI conversation begins a new conversation.

## 2. Modify Scenario

```{image} _static/screenshots/02-edit-scenario.png
:alt: Scene editor
:width: 100%
:align: center
```

The top controls include:

- **Draft box**: lists saved drafts, their update times, and configuration types. Select **Continue editing** to restore a draft, or delete it after confirmation.
- **Restore Defaults**: discard current scene edits after confirmation and reload the default configuration.
- **Save Changes**: save the current edits. **Unsaved changes** indicates edits that have not been saved.
- **Confirm & Continue**: save pending changes and proceed to agent configuration.

The **Scene List** shows the experiment's scenes. Select an item to view its title, description, **Call to Action**, and **Default Premise**. The action field specifies how agents should respond. The premise field records what each agent knows on entering that scene. If you switch scenes with unsaved edits, the platform prompts you to save.

### Custom interventions

The **AI Intervention Workshop** is separate from scenario creation. It is available for built-in and saved custom scenarios. On **Modify Scenario**, select **Custom intervention** in the Scene List to open it. An intervention adds an experimental condition to the existing scenario.

#### 1. Choose a recommendation or describe your own

The workshop shows **Participants you can use** and **Baseline scene order**. It offers scenario-specific suggestions at four levels: **Individual**, **Immediate circle**, **School**, and **Society**. Select a recommendation to build on, or choose **Design a new intervention condition** and describe your own in **What should the intervention do?**. Specify who acts, what they do, and when, then click **Send**.

```{image} _static/screenshots/intervention-workshop-input.png
:alt: Recommended interventions and the option to design a custom condition
:width: 100%
```

#### 2. Review and edit the generated canvas

Opening a recommendation displays its intervention canvas. Review the title, scene order, participants, rounds, role premises, and action task. Expand or scroll through the content and edit available fields. In the example, **Private Reflection Before Meeting** is a recommended individual intervention; inspect the displayed scene order and insertion point before saving.

```{image} _static/screenshots/intervention-generated-preview.png
:alt: Recommended intervention canvas with scene details, editable action task, and Save changes
:width: 100%
```

For a custom request, answer any follow-up questions and review the brief before generating it. Check that the actors, timing, and new scenes implement your intention. Use the conversation to request revisions when needed.

#### 3. Save and include the intervention in a run

Click **Save changes** in the recommendation canvas, or use the save control shown for a custom intervention. The saved intervention can then be reviewed from the scene editor. On the run page, select **Intervention simulation only** or **Original + Intervention simulation**, and check the selected interventions before starting.

You can return to the intervention workshop to review or revise saved interventions. Creating an intervention here does not require recreating the custom scenario.

## 3. Configure Agents

```{image} _static/screenshots/03-configure-roles.png
:alt: Agent configuration page
:width: 100%
:align: center
```

After **Confirm & Continue**, agents are grouped by the current run scope and scene.

> **Agent settings are shared across scenes.** Editing and saving an agent in any scene updates that agent throughout the experiment, including its goals, traits, known information, core needs, and social value orientation. To keep different settings for participants with the same name, use distinct agent identities; scene position alone does not distinguish them.

Cards summarize names, types, goals, and traits. **Edit** opens settings for goals, behavioral traits, known information, scene memories, tracked core needs and their initial values from 0 to 10, social needs, and social value orientation (SVO). Where supported, you can also provide custom value indicators and their JSON definitions.

Select at least one tracked core need before entering its initial value. Save in the dialog, then review the updated cards. The top **Draft box** can restore an agent-configuration draft; restoring defaults discards edits after confirmation. **Confirm & Continue** opens the run page.

## 4. Run Simulation

```{image} _static/screenshots/04-run-simulation.png
:alt: Three simulation run modes and real-time logs
:width: 100%
:align: center
```

Choose one of the three run modes:

- **Original simulation only**: run the baseline.
- **Intervention simulation only**: run the intervention branches.
- **Original + Intervention simulation**: run the baseline first, followed by each intervention branch.

Review the current mode and selected interventions before starting. Click the start button once. It changes to a stop button and the log refreshes automatically. Combined runs show phase markers for the baseline and intervention stages. Stop the run if needed.

When the run completes, **View Results** becomes available. Logs are organized by condition and scene, including steps, participants, and events. Search by keyword to locate an agent or event. Export the log to download a text copy. Processed logs also show condition counts, record counts, and empty-event counts.

## 5. Results Analysis

```{image} _static/screenshots/05-results-analysis.png
:alt: Results analysis and its main sections
:width: 100%
:align: center
```

Select **View Results** to enter the results workspace. **View Logs** returns to the run step; **Media Generation** opens step six; restarting clears the workflow after confirmation.

The page contains an overall process summary, agent-state analysis, **LLM Surveyor (Psychometric Results)**, and **LLM Rater (Behavior Analysis)**. Screenshots use existing local results to illustrate the controls. Conditions, agents, scales, and numbers are examples; use the data actually displayed for your run.

### Overall process and agent states

The process summary shows step, event, and scene counts, followed by a narrative. Condition buttons switch the summary to that condition. Older results may lack a saved summary. Agent-state analysis provides condition and agent selection, state summaries, curves, and core-need details.

```{image} _static/screenshots/09a-results-role-summary.png
:alt: Agent selection and state summary
:width: 100%
```

```{image} _static/screenshots/09b-results-role-detail.png
:alt: Value-gap curve and core-need details
:width: 100%
```

The images show the upper and lower parts of the same area:

1. Select a condition and then an agent.
2. Review need gaps, SVO, own satisfaction, and satisfaction with others, plus the largest-gap and largest-change indicators when available.
3. Switch the state metric and hover over a curve point to read its value at that step.
4. Review initial, final, expected, gap, and change values in the core-need details. Select **View Logs** for full events.

A need gap is the expected value minus the current value. Satisfaction indicators come from simulated state records; the indicator concerning others reflects the agent's estimate of others' states. These indicators are separate from questionnaire scores.

### Surveyor: psychometric results

Expand **LLM Surveyor (Psychometric Results)**. Results are grouped by condition and questionnaire. Cards show available target agents, item counts, summary metrics, dimensions, scale descriptions, and interpretations. If there are no corresponding measurements, the page shows a no-data message. This area displays results, not questionnaire configuration.

```{image} _static/screenshots/10a-results-surveyor-baseline.png
:alt: Surveyor results grouped by baseline and intervention
:width: 100%
```

For comparison, locate the same scale, agent, and metric in each condition. Read the scale description to establish score direction before comparing totals, means, or dimension scores. Expand detailed records or **Surveyor Answers** when provided, and click again to collapse them. Available controls depend on the measurement's data structure.

### Rater: behavioral analysis

Expand **LLM Rater (Behavior Analysis)**. Select an agent with available logs or measurement results, select one or more configured rating tools, and run the rating. Cards are grouped by condition and may include hit counts, mean scores, mean severity, principal agents, record or field counts, and representative evidence.

```{image} _static/screenshots/11a-results-rater-baseline.png
:alt: Rater results grouped by baseline and intervention
:width: 100%
```

Check the target and tool before running the rating, then inspect the condition-specific summaries and evidence. Hit counts are records identified under that tool. Compare mean scores and severity only under the same criteria and direction. Zero hits means the current logs contain no clearly identified matching records; it does not by itself establish intervention success or failure. Open detailed evidence only when the result provides it, and check full logs for context.

### Conditions, logs, and missing results

Condition buttons switch the agent-state view; Surveyor and Rater use their own condition groups. Check each area separately and compare the same agent and measurement tool. Return through **View Logs** to search or export logs, then **View Results** to continue analysis.

If no results exist, complete a run or open one from history. If only one area is empty, check whether that run saved the relevant summary or measurements. To obtain behavioral ratings, select an agent and criteria in Rater and run the rating.

## 6. Media Generation

```{image} _static/screenshots/06-media-generation.png
:alt: Comic and video generation
:width: 100%
:align: center
```

Open **Media Generation** from results or step six. **View Results** returns to analysis; restarting returns to scenario selection after confirmation. Media uses the currently selected result condition.

### Comics

Submit a comic-generation task. The page shows queueing, story analysis, and image-generation states. When complete, view or download the image. Multiple generations for a condition can be retained and selected. Administrators who see the save-all-prompts option can enable it before generation, then download the prompts afterward.

### Video prompts and videos

Generate video prompts first. Review available prompt history and download the prompt JSON if needed. Check the prompts and condition, then submit video generation. On completion, a video player and download link appear.

If structured event logs are unavailable, the platform cannot generate prompts. Rerun the simulation to obtain the required logs.

## Drafts, history, and recovery

The scene and agent editors' **Draft box** stores in-progress configurations. The platform attempts to autosave drafts before navigation or refresh. **Continue editing** reloads the scenario. Autosaved drafts show their update time and expiry: they are deleted after three days. Manually saved drafts remain until deleted, so save explicitly for long-term retention.

Open completed runs through simulation history. Each record shows its scenario, mode, and time. Select a record to reopen its saved results, logs, and configuration snapshot without rerunning. Surveyor, Rater, and media tools remain available for the saved conditions where supported.

See [Results and Measurements](results-and-measurements.md) and [Getting Started](quickstart.md).
