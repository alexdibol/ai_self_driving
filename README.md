# The Self-Driving Project
## From Control to Financial Judgment

**Author: Alejandro Reynoso**

Four interactive laboratories explore how autonomous systems combine perception, quantitative analysis, contextual judgment, governed execution, and feedback. The journey moves from a self-driving racing car to air traffic control, dynamic logistics, and cybersecurity—then examines how the same architecture can inform trading, portfolio coordination, capital allocation, and systemic-risk management.

The central proposition is **control with judgment**. Deterministic algorithms provide measurement, prediction, optimization, feasibility checks, and fast control. A bounded language-model supervisor contributes contextual interpretation when conditions change or objectives conflict. Independent governance determines which recommendations may become actions.

## Start here: the main document

[**Self-Driving Models: From Control to Financial Judgment — complete synthesis (PDF)**](THE%20SELF%20DRIVING%20LAB.pdf)

The main document connects the four laboratories into a unified research program. It develops the canonical architecture, explains the boundary between optimization and judgment, maps the experiments to financial institutions, and sets out a research and business-validation agenda.

**Suggested path:** read the synthesis, study each laboratory's monograph, use its slides to review the architecture, and run its notebook to inspect decisions and outcomes.

## Laboratory materials

Each laboratory includes a monograph, a slide deck, and an interactive notebook. The Colab links open the actual notebooks hosted in this repository.

| Laboratory | Monograph | Slides | Notebook on GitHub | Run in Google Colab |
|---|---|---|---|---|
| **1. Self-driving racing car** | [Read PDF](lab_1/self_driving_race_car_monograph.pdf) | [View deck](lab_1/self_driving_car_slides.pdf) | [View notebook](lab_1/self_driving_car_colab_notebook_github.ipynb) | [Open in Colab](https://colab.research.google.com/github/alexdibol/ai_self_driving/blob/main/lab_1/self_driving_car_colab_notebook_github.ipynb) |
| **2. Air traffic control** | [Read PDF](lab_2/self_driving_air%20_traffic_control.pdf) | [View deck](lab_2/self_driving_air_traffic_control_slides.pdf) | [View notebook](lab_2/self_driving_air_traffic_control_colab_notebook.ipynb) | [Open in Colab](https://colab.research.google.com/github/alexdibol/ai_self_driving/blob/main/lab_2/self_driving_air_traffic_control_colab_notebook.ipynb) |
| **3. Dynamic logistics** | [Read PDF](lab_3/self_driving_logistics_light.pdf) | [View deck](lab_3/self_driving_logistics_slides_text.pdf) | [View notebook](lab_3/self_driving_logistics_colab_notebook.ipynb) | [Open in Colab](https://colab.research.google.com/github/alexdibol/ai_self_driving/blob/main/lab_3/self_driving_logistics_colab_notebook.ipynb) |
| **4. Cybersecurity, propagation, and cyber risk** | [Read PDF](lab_4/self_driving_cybersecurity.pdf) | [View deck](lab_4/self_driving_cybersecurity_slides.pdf) | [View notebook](lab_4/self_driving_cybersecurity_colab_notebook.ipynb) | [Open in Colab](https://colab.research.google.com/github/alexdibol/ai_self_driving/blob/main/lab_4/self_driving_cybersecurity_colab_notebook.ipynb) |

### Laboratory 1 — Self-driving racing car: adaptation

A vehicle navigates a simplified Autódromo Hermanos Rodríguez while coping with changing grip, curves, obstacles, and imperfect sensors. The experiment separates observations from estimated state, fast feedback control from slower supervisory judgment, and recommended behavior from authorized actuator commands.

**Key question:** how should a system adjust its behavior when uncertainty or environmental conditions change?

The safety governor checks proposed behavior against deterministic limits before execution. Students can inspect the information flowing between sensors, estimation, supervision, governance, and vehicle dynamics.

**Finance transfer:** a research analogy for regime-sensitive trading execution and risk adjustment, where fast numerical control operates inside limits and contextual supervision can reconsider policy.

### Laboratory 2 — Air traffic control: coordination

A synthetic approach-control environment coordinates sixty aircraft across MEX, NLU, and TOL. Weather, wind, congestion, and interacting trajectories create a system-wide allocation problem. Perception, prediction, sequencing, and a bounded supervisory layer cooperate through a deterministic validation harness.

**Key question:** how can an autonomous system coordinate many interacting agents when a local decision changes conditions for others?

The laboratory extends the single-vehicle loop into a network. It makes visible the difference between an individually attractive action and a feasible coordinated response.

**Finance transfer:** a research analogy for coordinating portfolios, markets, and balance sheets when exposures, constraints, and interventions interact.

### Laboratory 3 — Dynamic logistics: priorities and triage

A synthetic delivery company manages vehicles, packages, capacities, deadlines, and disruptions. Traffic, weather, vehicle failures, and urgent shipments force repeated reassignment and reprioritization. Deterministic analysis generates feasible alternatives; Claude Haiku 4.5 provides bounded supervisory judgment; validation controls execution.

**Key question:** which commitment should receive scarce resources when efficiency, urgency, resilience, and service obligations conflict?

This laboratory exposes the distinction between calculating a feasible plan and interpreting what matters under exceptional circumstances. Outcomes and audit records make the consequences of those choices inspectable.

**Finance transfer:** a research analogy for allocating capital, liquidity, or collateral under competing obligations and changing priorities.

### Laboratory 4 — Cybersecurity: propagation and operational risk

A synthetic Security Operations Center models enterprise assets and their dependencies. Telemetry becomes evidence, threat assessment considers propagation, and defensive decisions weigh confidence, criticality, operational impact, and reversibility. Governance distinguishes automatically permitted interventions from actions requiring escalation.

**Key question:** when should a system intervene when both acting and waiting have costs?

Containing a threat may interrupt a critical service; preserving service may allow risk to spread. The laboratory therefore evaluates cyber defense as an operational judgment problem with system-wide consequences.

**Finance transfer:** a research analogy for contagion-aware systemic-risk monitoring and interventions that balance local containment with institutional continuity.

## One architecture, four increasing challenges

The shared loop is:

**Environment → Perception and state estimation → Analysis and prediction → Bounded judgment → Governance and validation → Execution → Feedback → Updated environment**

| Component | Responsibility |
|---|---|
| Perception and estimation | Turn observations into an operational state, including uncertainty. |
| Analysis and prediction | Calculate consequences, constraints, risks, and feasible alternatives. |
| Judgment | Interpret circumstances and reconcile competing priorities within delegated bounds. |
| Governance and validation | Enforce limits, verify admissibility, and require escalation where appropriate. |
| Execution | Apply authorized actions to the simulated world. |
| Feedback and memory | Record outcomes and inform the next decision cycle. |

The pedagogical progression is **adaptation → coordination → reprioritization → propagation-aware intervention**. Across all four laboratories, a recommendation acquires execution authority only through the appropriate control boundary.

## Learning objectives and teaching method

The materials are intended for financial practitioners, executives, advanced students, and instructors studying autonomous systems and institutional design.

By working through the laboratories, readers should be able to:

- Explain how classical control, optimization, and generative reasoning complement one another.
- Distinguish observations, estimates, recommendations, authorized actions, and realized outcomes.
- Identify when contextual judgment adds a distinct role beyond numerical calculation.
- Design bounded supervisory roles, validation gates, escalation paths, and observable feedback.
- Formulate testable hypotheses for transferring the architecture to financial decisions.

The monographs explain the conceptual problem; the slides support teaching and discussion; the notebooks expose the architecture through executable simulations, explanatory text, visualizations, and experiments.

## Running the notebooks

1. Choose **Open in Colab** in the materials table and save a personal copy if you want to retain changes.
2. Read the introduction and configuration cells, then execute the notebook in order.
3. For Claude-enabled experiments, configure the Colab secret named exactly `ANTHROPIC_API_KEY` and enable notebook access.
4. Review model settings, governance rules, and outputs before changing experiment parameters.

The laboratories have different LLM startup policies. **The current logistics notebook requires a working Claude connection at startup** through `USE_CLAUDE=True` and `REQUIRE_CLAUDE=True`. The air traffic notebook supports deterministic fallback when Claude is unavailable, and the cybersecurity notebook sets `USE_LLM=False` by default. Consult each notebook's configuration rather than assuming identical behavior across laboratories. Live model calls may incur provider charges.

## Research scope

These are synthetic pedagogical simulations. The financial mappings are research propositions requiring independent testing against quantitative, rule-based, and human baselines. The project does not report empirical financial superiority.

The notebooks are teaching tools for examining architecture and governance; they are not operational vehicle-control, aviation, logistics, cybersecurity, or investment systems.

## Authorship and AI assistance

**Alejandro Reynoso** is the author and is responsible for the project's direction, conceptual architecture, editorial construction, pedagogical structure, selection and integration of examples, and final content.

AI tools were used to assist with code generation, writing, revision, and preparation of supporting materials. That assistance does not transfer authorship or responsibility to an AI system. Intellectual direction, editorial decisions, pedagogical design, and responsibility for the published work remain with Alejandro Reynoso.

## License and copyright

Copyright © 2026 Alejandro Reynoso.

This repository's original code and authored materials are released under the **MIT License**. See [LICENSE](LICENSE) for the complete terms. Any third-party materials retain their respective rights and license terms.
