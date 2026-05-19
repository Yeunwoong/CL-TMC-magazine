# IV. Use Cases of CL-TMC (Skeleton)

This section illustrates two representative instantiations of CL-TMC: heterogeneous multi-modal sensing control for localization and domain-specific multi-channel sensing control for biomedical prediction. Together, these examples show how the same closed-loop principle can be specialized across different task domains while preserving a common architecture.

Figure 2 is presented as a combined use-case figure with two representative instantiations: Figure 2(a) for localization and Figure 2(b) for biomedical prediction.

## IV-A. Use Case 1: Energy-Efficient Localization

Localization tasks can operate under different quality requirements depending on the service context, user state, and environment. For instance, coarse positioning may be sufficient for some services, while others require tighter localization quality with lower uncertainty.

In a CL-TMC setting, sensing and communication effort should therefore adapt to the required localization quality rather than follow a fixed one-size-fits-all policy. The controller can adjust modality activation and sensing rates across GNSS, cellular, Wi-Fi, BLE, IMU, and environmental sensing based on quality targets, uncertainty, energy state, and network context.

The expected outcome is improved tradeoff behavior: unnecessary sensing/communication overhead can be reduced when quality requirements are moderate, while additional sensing effort can be allocated when higher localization quality is required.

**Citation needs:** [REF NEEDED: network-assisted localization], [REF NEEDED: multi-modal localization], [REF NEEDED: energy-aware localization sensing].

## Figure 2(a) Placeholder

**[Figure 2(a) about here: Energy-efficient localization architecture]**

**Caption skeleton:** CL-TMC instantiation for localization, where task-level localization quality feedback controls future sensing modality/rate decisions.

---

## IV-B. Use Case 2: Multi-Channel Biomedical Prediction

Biomedical prediction pipelines in wearable or edge-assisted settings may rely on multi-channel physiological sensing (for example, ECG-centered channel sets). Different channels can carry different signal characteristics, and their contribution to prediction can vary with context and task state.

Under CL-TMC, the sensing controller uses task-level indicators such as prediction confidence, uncertainty, or error to adapt channel activation and sampling intensity over time. This avoids relying on fixed all-channel high-rate collection when it is not necessary for the target task.

The expected result is a better task-cost balance in which sensing and communication overhead are reduced while maintaining task-relevant prediction performance.

**Citation needs:** [REF NEEDED: multi-channel biomedical sensing], [REF NEEDED: channel selection for ECG/EEG], [REF NEEDED: wearable prediction under resource constraints].

## Figure 2(b) Placeholder

**[Figure 2(b) about here: Multi-channel biomedical prediction architecture]**

**Caption skeleton:** CL-TMC instantiation for biomedical prediction, where task-level prediction indicators drive channel/sampling adaptation.

---

## IV-C. Cross-Use-Case Synthesis

Across both use cases, the structural pattern is identical: task outcomes are measured, fed back, and used to adapt sensing actions under constraints. What changes by domain are modality choices, constraints, and evaluation metrics—not the core CL-TMC principle.

The same principle can be extended to other sensing-intensive applications, including mobility prediction, digital twin updates, and context-aware services.

**Citation needs:** [REF NEEDED: cross-domain adaptive sensing frameworks].

## Figure 3 Placeholder (Localization Performance Illustration)

**[Figure 3 about here: Localization performance-cost tradeoff]**

**Caption skeleton:** Example evaluation illustrating the tradeoff between localization task performance and sensing/communication cost under static policies versus CL-TMC-style adaptive control.

## Figure 4 Placeholder (Biomedical Performance Illustration)

**[Figure 4 about here: Biomedical prediction performance-cost tradeoff]**

**Caption skeleton:** Example evaluation illustrating the tradeoff between biomedical prediction task performance and sensing/communication cost under fixed-channel policies versus CL-TMC-style adaptive control.
