# I. Introduction (Skeleton)

## Paragraph 1 — Sensing-Intensive IoT Context

Future IoT systems are evolving from simple data collection platforms into sensing-intensive task processing systems. Instead of only uploading raw measurements, these systems are increasingly expected to support application-level outcomes such as localization, digital twins, XR/context-aware services, autonomous operation, and smart healthcare workflows under dynamic constraints.

**Citation needs:** [REF NEEDED: sensing-intensive IoT applications overview], [REF NEEDED: evolution from data collection to task-oriented IoT systems].

## Paragraph 2 — Why Multi-Modal Sensing is Needed

A single sensing source is often insufficient because different modalities provide complementary observations and have different robustness, energy, and coverage properties. For example, localization can combine GNSS, cellular, Wi-Fi, BLE, IMU, and environmental sensing to improve operational robustness across conditions. Similarly, biomedical prediction can rely on multi-channel ECG or other physiological sensing channels, where different channels may capture different task-relevant signal characteristics.

In this manuscript, **multi-modal sensing** is the primary terminology. **Multi-channel sensing** is treated as a special case or domain-specific extension where multiple homogeneous or domain-specific channels are selectively controlled for a task.

**Citation needs:** [REF NEEDED: multi-modal sensing and sensor fusion in IoT], [REF NEEDED: heterogeneous localization sensing modalities], [REF NEEDED: multi-channel physiological sensing for biomedical prediction].

## Paragraph 3 — Limits of Static/Data-Centric Collection

Prior work has made important progress through sleep scheduling, duty cycling, adaptive sampling, and redundancy-aware sensing, and these methods remain valuable for reducing sensing and communication overhead. However, many such approaches primarily optimize sensor/network-level efficiency metrics (e.g., energy consumption, duty ratio, traffic load, and coverage) rather than explicitly using task-performance feedback to control sensing actions.

**Citation needs:** [REF NEEDED: sleep scheduling and duty cycling in IoT/WSN], [REF NEEDED: adaptive sampling and redundancy-aware sensing], [REF NEEDED: sensor/network-level efficiency metrics in sensing systems].

## Paragraph 4 — Core Shift to CL-TMC

This motivates a key design question: Which sensing data are necessary to meet a target task requirement under current system conditions?

To address this question, we center on the **closed-loop framework for task-aware multi-modal sensing control (CL-TMC)**, where task-level indicators (e.g., error, confidence, uncertainty, or QoE) are fed back to adapt modality selection, sensing frequency, and transmission behavior over time.

**Citation needs:** [REF NEEDED: task-oriented communication or goal-oriented system design], [REF NEEDED: closed-loop task-feedback control principle].

## Paragraph 5 — Contributions (Skeleton Bullets)

- We present CL-TMC as a closed-loop framework linking task outcomes and sensing control.
- We identify key control dimensions: modality/channel selection, sensing frequency, data representation/reduction, and communication-aware adaptation.
- We map CL-TMC to representative use cases: energy-efficient localization and multi-channel biomedical prediction.
- We identify open research issues spanning task-performance modeling, methodology selection, dataset/evaluation methodology, network-assisted feedback design, scalability, and practical deployment.

**Citation needs:** [REF NEEDED: prior frameworks for adaptive sensing control].

## Paragraph 6 — Paper Roadmap

Section II motivates the transition from data-centric collection to task-aware closed-loop control. Section III details the CL-TMC architecture. Section IV presents representative use cases. Section V discusses open issues. Section VI concludes.
