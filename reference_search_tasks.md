# Reference Search Tasks for CL-TMC Manuscript Skeleton

Because `references.bib` is currently empty, this file lists prioritized literature search tasks needed to replace `[REF NEEDED: ...]` placeholders.

## Priority Legend

- **High:** needed to support core framing and CL-TMC differentiation.
- **Medium:** strengthens technical context and use-case grounding.
- **Low:** useful for breadth in open-issues discussion.

---

## 1) Introduction Support (High)

1. Find recent surveys/tutorials on sensing-intensive IoT and context-aware services.
2. Find representative multi-modal sensing/sensor fusion references for IoT.
3. Find works discussing limitations of static/fixed sensing pipelines.
4. Find task-oriented/goal-oriented/semantic communication references that support the shift from data-centric to task-centric design.

---

## 2) Background and Differentiation Support (High)

1. Sleep scheduling, duty cycling, and energy-efficient sensor activation in WSN/IoT.
2. Adaptive sampling and sampling-rate control references.
3. Data reduction and feature-reporting references (including compressed sensing as one option).
4. Redundancy-aware or correlation-aware sensing/data collection references.
5. Sources that help articulate why task-level feedback is a distinct design axis beyond sensor/network metrics.

---

## 3) Framework Section Support (High)

1. Cross-layer sensing-communication-task co-design references.
2. Task-level performance metric design references (uncertainty/confidence/QoE in sensing-driven systems).
3. Feedback-driven adaptive sensing control architectures.
4. Methodology references: rule-based, optimization-based, online learning/bandits, RL (balanced coverage).

---

## 4) Use Case Support (High/Medium)

### Localization (High)

1. Network-assisted localization references spanning GNSS/cellular/Wi-Fi/BLE/IMU fusion.
2. Energy-aware localization sensing/control references.
3. Practical uncertainty-aware localization evaluation references.

### Biomedical prediction (High)

1. Multi-channel physiological sensing (ECG/EEG-centric) references.
2. Channel selection under resource constraints.
3. Wearable sensing and communication overhead tradeoff references.

### Cross-use-case synthesis (Medium)

1. Cross-domain adaptive sensing framework papers demonstrating reusable control principles.

---

## 5) Open Issues Support (Medium/Low)

1. Delayed/noisy feedback and control stability references.
2. Edge-cloud partitioning for sensing/inference pipelines.
3. Benchmarking methodologies jointly reporting task metrics + resource overhead.
4. Privacy/security for adaptive/task-aware sensing pipelines.
5. Interoperability and standardization references for IoT sensing-control interfaces.

---

## 6) Curation Rules for Populating `references.bib`

- Prefer high-quality surveys + seminal papers + recent representative systems papers.
- Ensure every placeholder in manuscript files is mapped to at least one candidate citation.
- Maintain methodological balance; do not over-concentrate on reinforcement learning papers.
- Include compressed sensing references only as part of a broader data-reduction context.
- Avoid adding references that reposition the manuscript away from CL-TMC centrality.
