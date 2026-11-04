# Getting Started

EduMirror is an online platform for exploring and analyzing educational scenarios. Start with a provided scenario, review its agents, relationships, and experimental conditions, then run a simulation to observe changes in behavior and simulated psychological states.

Compare baseline and intervention conditions to examine interaction processes, core-need satisfaction, satisfaction indicators, and social value orientation. After a run, inspect the interaction record, agent states, Surveyor questionnaires, and Rater behavioral analysis. You can also generate comics or videos.

Scenarios cover situations such as peer relationships, bullying, family communication, and school activities. The illustration below shows participants with different roles and relationships; the platform records their actions and state changes during simulation.

```{image} _static/scenario-bullying.jpg
:alt: Illustration of an educational scenario
:width: 70%
:align: center
```

## Sign in

Open the platform and sign in with your registered email address or verified phone number and password. If you do not have an account, select registration. Email registration follows the application, review, and email-activation process; phone registration is completed after SMS verification.

After sign-in, the top of the page shows the interface language, account status, and remaining run allowance. Select **English** to follow the English controls in this guide.

```{image} _static/screenshots/00-login.png
:alt: Sign-in page in English
:width: 40%
:align: center
```

If you forget your password, use the password-reset option and choose email or SMS verification. **Continue with Guest** uses Beijing Normal University’s campus single sign-on system.

## The six steps

```{image} _static/screenshots/00-steps.png
:alt: Six-step navigation in English
:width: 100%
:align: center
```

1. Select Scenario
2. Modify Scenario
3. Configure Agents
4. Run Simulation
5. Results Analysis
6. Media Generation

Work from left to right. Use the step bar or the back button to revisit completed steps.

### 1. Select Scenario

Search by scenario name or keyword, or browse the scenario cards and choose one to continue.

```{image} _static/screenshots/01-select-scenario.png
:alt: Scenario selection page
:width: 100%
:align: center
```

- **Step bar**: shows your position and the remaining steps.
- **Search box**: filters scenarios by name or keyword.
- **Scenario cards**: show a brief description and let you select a scenario.
- **Pagination**: moves between pages of cards.

Read the brief description before opening a scenario to review its conditions and agents.

### 2. Modify Scenario

Review the scenario background, participants, interaction requirements, and conditions to check that they match your goal.

```{image} _static/screenshots/02-edit-scenario.png
:alt: Scenario editor
:width: 85%
:align: center
```

1. **Top controls**: check the scenario source. Use **Draft box**, **Restore Defaults**, **Save Changes**, and **Confirm & Continue**. Save edits before continuing.
2. **Scene List**: select a scene or condition to inspect. The baseline shows the process without added intervention; other conditions support comparison. The custom-intervention entry lets you add a condition while retaining the existing branches.
3. **Scene content**: review the title, description, and **Call to Action**, which specifies how agents should respond and what must remain unchanged.
4. **Default Premise**: enter what each agent already knows when entering this scene. Different agents can have different information, affecting their judgments and responses.

Review the baseline and intervention settings separately so you understand what changes between conditions. Save before proceeding.

### 3. Configure Agents

Agents are grouped by condition and scene for the current run scope. If an agent appears in several scenes, editing it updates the shared settings throughout the scenario.

```{image} _static/screenshots/03-configure-roles.png
:alt: Agent configuration page
:width: 100%
:align: center
```

1. Check the current run scope at the top.
2. Review each scene's name, description, and participants; the groups represent different scenes, not one conversation.
3. Read the agents' names, types, goals, and behavioral traits.
4. Click **Edit** to change the relevant goals, traits, known information, value orientation, or core needs.
5. Save in the editor, check the updated cards, then select **Confirm & Continue**. Use the restore-defaults control to discard edits when needed.

Agent settings influence actions and interactions. Check the baseline first, then make only the changes needed for your comparison.

### 4. Run Simulation

Choose **Original simulation only** for a baseline run. Save an intervention through the workshop before selecting **Intervention simulation only** or **Original + Intervention simulation**.

```{image} _static/screenshots/04-run-simulation.png
:alt: Original, intervention-only, and combined run modes
:width: 100%
:align: center
```

The combined mode runs the original simulation first and then each intervention branch. Check the selected mode and conditions before starting.

Check **Current Mode** and the listed conditions before starting. Click the start button once. It becomes a stop button during execution, while the log updates automatically. After completion, select **View Results**.

### 5. Results Analysis

```{image} _static/screenshots/05-results-analysis.png
:alt: Results analysis page
:width: 100%
:align: center
```

1. Read the overall process summary and consult the original event log as needed.
2. Examine agent-state changes: need gaps, social value orientation (SVO), satisfaction, and actions over global steps.
3. Expand **LLM Surveyor (Psychometric Results)** for questionnaire and structured measurement results.
4. Expand **LLM Rater (Behavior Analysis)** for behavioral evidence and scores derived from the logs.

If no results are available, the run may not have completed or its results may have been cleared. Run a simulation or open a saved record from history.

When comparing conditions, use the baseline as a reference and check the logs to understand how differences arose.

### 6. Media Generation

Select **Media Generation** from the results page.

```{image} _static/screenshots/06-media-generation.png
:alt: Media generation page
:width: 100%
:align: center
```

- **Comics**: generate a comic from the current simulation results.
- **Video**: generate video prompts, then submit a video-generation task.

Check the selected condition before submitting. Generation takes time and the page displays task status. A completed simulation is needed for usable media results.

## Practical tips

For your first run, choose a built-in scenario and select **Original simulation only**. Once logs and results are available, try editing agents and adding interventions.

- Save changes to scenes and agents.
- Keep baseline results when comparing interventions.
- Do not repeatedly click the start button while a run is in progress.

See [API Settings](api-settings.md) to configure model or media-generation services.
