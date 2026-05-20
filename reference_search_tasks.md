# Student Assignment: Reference Search Tasks for CL-TMC Manuscript

This assignment converts manuscript citation gaps into structured reference-search tasks. Use the current manuscript skeleton as context:

- `manuscript/introduction.md`
- `manuscript/background.md`
- `manuscript/framework.md`
- `manuscript/use_cases.md`
- `manuscript/open_issues.md`

## Rules

1. **Do not invent citations.**
2. **Do not add specific paper titles unless already present in `references.bib`.**
3. **Do not search outside the assigned topics.**
4. **Do not treat privacy/security as a major category for this assignment.**
5. For every selected paper, provide the required output format exactly.

---

## Required Output Format (for every paper you submit)

For each paper you collect, submit:

1. **BibTeX entry**
2. **3–5 sentence summary**
3. **Key technical point** (1–2 sentences)
4. **How it supports CL-TMC** (1–2 sentences)
5. **Difference from CL-TMC (if applicable)** (1–2 sentences)

---

## Task 1

- **Topic:** Sensing-intensive IoT and context-aware services
- **Manuscript location:** `manuscript/introduction.md` (Paragraph 1), `manuscript/use_cases.md` (Section IV opening)
- **Claim that needs support:** Future IoT systems are evolving from simple data collection toward sensing-intensive, task-processing, context-aware services.
- **What type of source to find:** Recent survey/tutorial + representative systems papers
- **Required number of papers:** 4
- **Required student output:** Use the required output format above for each paper.

## Task 2

- **Topic:** Multi-modal sensing and sensor fusion
- **Manuscript location:** `manuscript/introduction.md` (Paragraph 2), `manuscript/framework.md` (III-B.1)
- **Claim that needs support:** Heterogeneous sensing modalities provide complementary information and improve robustness compared with single-source sensing.
- **What type of source to find:** Survey papers + representative application/system papers
- **Required number of papers:** 5
- **Required student output:** Use the required output format above for each paper.

## Task 3

- **Topic:** Task-oriented / semantic communication
- **Manuscript location:** `manuscript/introduction.md` (Paragraph 4), `manuscript/background.md` (II-E)
- **Claim that needs support:** System design should prioritize task usefulness of information rather than data delivery alone.
- **What type of source to find:** Conceptual/framework papers + recent overviews
- **Required number of papers:** 4
- **Required student output:** Use the required output format above for each paper.

## Task 4

- **Topic:** Energy-efficient sensing (sleep scheduling, duty cycling, sensor activation)
- **Manuscript location:** `manuscript/background.md` (II-B)
- **Claim that needs support:** Sleep scheduling/duty cycling/sensor activation reduce energy use and improve coverage/connectivity/lifetime, but may not directly optimize task-level inference quality.
- **What type of source to find:** Foundational methods + representative modern IoT implementations
- **Required number of papers:** 5
- **Required student output:** Use the required output format above for each paper.

## Task 5

- **Topic:** Adaptive sampling and data reduction
- **Manuscript location:** `manuscript/background.md` (II-C), `manuscript/framework.md` (III-C)
- **Claim that needs support:** Adaptive sampling and data reduction can reduce sensing/communication cost; compressed sensing is one option but not the full task-aware framework.
- **What type of source to find:** Adaptive sampling papers + data representation/reduction papers (including compressed sensing as a subset)
- **Required number of papers:** 5
- **Required student output:** Use the required output format above for each paper.

## Task 6

- **Topic:** Redundancy-aware sensing
- **Manuscript location:** `manuscript/background.md` (II-D)
- **Claim that needs support:** Statistical redundancy/correlation is useful for pruning data, but redundancy is not always equivalent to task irrelevance.
- **What type of source to find:** Correlation-aware sensing/data collection papers + analyses of task relevance limits
- **Required number of papers:** 4
- **Required student output:** Use the required output format above for each paper.

## Task 7

- **Topic:** Network-assisted localization
- **Manuscript location:** `manuscript/introduction.md` (Paragraph 2 example), `manuscript/use_cases.md` (IV-A)
- **Claim that needs support:** Localization benefits from combining GNSS/cellular/Wi-Fi/BLE/IMU and adapting sensing effort to required localization quality.
- **What type of source to find:** Multi-modal localization methods + network-assisted localization system studies
- **Required number of papers:** 6
- **Required student output:** Use the required output format above for each paper.

## Task 8

- **Topic:** Multi-channel biomedical sensing
- **Manuscript location:** `manuscript/introduction.md` (Paragraph 2 biomedical example), `manuscript/use_cases.md` (IV-B)
- **Claim that needs support:** Multi-channel physiological sensing can improve prediction, and channel/sampling adaptation can reduce overhead while maintaining target prediction quality.
- **What type of source to find:** Multi-channel ECG/physiological sensing papers + channel selection/resource-aware monitoring studies
- **Required number of papers:** 6
- **Required student output:** Use the required output format above for each paper.

## Task 9

- **Topic:** Methodology selection (rule-based, optimization-based, online learning, contextual bandits, reinforcement learning)
- **Manuscript location:** `manuscript/open_issues.md` (V-B)
- **Claim that needs support:** Different control methodologies have different tradeoffs in interpretability, complexity, online/offline operation, data requirements, and adaptability.
- **What type of source to find:** Comparative/control-method papers; include at least one source per methodology family
- **Required number of papers:** 8 (minimum distribution: 1 rule-based, 2 optimization-based, 2 online learning/bandits, 3 RL)
- **Required student output:** Use the required output format above for each paper.

## Task 10

- **Topic:** Edge/cloud deployment and standardization/interoperability
- **Manuscript location:** `manuscript/open_issues.md` (V-E, V-F), `manuscript/framework.md` (III-B.2)
- **Claim that needs support:** Practical CL-TMC deployment requires device-edge-cloud partitioning and standardized interfaces for sensing capabilities/costs, feedback signals, network telemetry, and control commands.
- **What type of source to find:** Edge-cloud systems papers + standards/interoperability framework papers
- **Required number of papers:** 5
- **Required student output:** Use the required output format above for each paper.

---

## Submission Checklist (Student)

- [ ] I followed the required output format for every paper.
- [ ] I did not invent citations.
- [ ] I did not include unverified bibliographic metadata.
- [ ] I mapped each paper to at least one specific manuscript location.
- [ ] I explained how each paper supports CL-TMC and, when relevant, how it differs from CL-TMC.

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
