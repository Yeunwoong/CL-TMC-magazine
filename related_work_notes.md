# Related Work Notes

## Purpose

This file summarizes the categories of related work that should be used in the article. The goal is not to write a full literature survey, but to clarify how prior studies support the motivation of CL-TMC and how the proposed framework is differentiated from them.

The article should position CL-TMC as a closed-loop framework that extends existing sensor/network-level efficiency approaches toward task-performance-feedback-based sensing control.

---

## 1. Multi-Modal Sensing and Sensor Fusion

### Role in This Article

These works are used to motivate why future IoT systems require heterogeneous sensing data.

### Expected Use

Use these references in the Introduction and Section II to explain that different sensors observe different physical phenomena and provide complementary features. A single sensing source may be insufficient because each modality has different strengths and limitations in terms of accuracy, robustness, coverage, energy consumption, and environmental dependency.

### Example Discussion

Localization may rely on GNSS, cellular, Wi-Fi, BLE, IMU, and environmental sensors. GNSS is useful outdoors but can be unreliable indoors or in urban canyons. Wi-Fi and BLE can provide useful indoor signals, while IMU can provide short-term motion information. Therefore, multi-modal sensing can improve task robustness by combining complementary observations.

### Differentiation

Existing multi-modal sensing and fusion studies mainly focus on improving task accuracy or robustness by using multiple sensing sources. CL-TMC focuses on controlling which modalities should be activated, how frequently they should be used, and how much sensing data should be transmitted according to task-level feedback.

### Candidate References

- Multi-modal sensor fusion for IoT systems
- Multi-modal localization using wireless and inertial signals
- Sensor fusion for context-aware computing
- Multi-modal sensing for digital twins or XR systems

---

## 2. Task-Oriented and Semantic Communication

### Role in This Article

These works are used to support the high-level shift from data-centric communication to task-oriented system design.

### Expected Use

Use these references to explain that future communication and sensing systems should not be optimized only for bit-level reconstruction or raw data delivery. Instead, they should consider whether the delivered data are useful for the target task.

### Example Discussion

Task-oriented communication and semantic communication emphasize that the goal of communication is not always to reconstruct all transmitted data, but to support the intended task or meaning at the receiver. This perspective is aligned with CL-TMC because CL-TMC determines sensing actions based on task-level performance rather than raw data availability.

### Differentiation

Task-oriented communication mainly focuses on what information should be transmitted for a given task. CL-TMC extends this idea to sensing control by asking what sensing data should be collected, when they should be collected, and how they should be delivered.

### Candidate References

- Task-oriented communication
- Semantic communication
- Goal-oriented communication
- Edge intelligence for task-oriented inference

---

## 3. Energy-Efficient Sensing and Sleep Scheduling

### Role in This Article

These works are used to acknowledge existing studies that reduce sensing energy in wireless sensor networks and IoT systems.

### Expected Use

Use these references in Section II-B to explain that energy-efficient sensing has been widely studied through sleep scheduling, duty cycling, sensor activation control, and energy-aware data collection.

### Example Discussion

Sleep scheduling and duty cycling reduce energy consumption by allowing sensor nodes to alternate between active and sleep states. Sensor activation control determines which sensors should remain active to satisfy coverage or connectivity requirements. These approaches can extend network lifetime and reduce unnecessary sensing operations.

### Differentiation

These studies mainly optimize sensor-level or network-level metrics such as energy consumption, coverage, connectivity, and network lifetime. CL-TMC differs by explicitly using task-performance feedback, such as localization accuracy or prediction confidence, to control sensing operations.

### Candidate References

- Sleep scheduling in wireless sensor networks
- Duty cycling for energy-efficient IoT sensing
- Sensor activation control
- Energy-aware routing and data collection

---

## 4. Adaptive Sampling and Data Reduction

### Role in This Article

These works are used to explain existing approaches that reduce the amount of sensing data.

### Expected Use

Use these references in Section II-C and Section III-C to discuss adaptive sampling, sampling rate control, selective data acquisition, sparsity-aware sensing, feature reporting, and compressed sensing as possible data reduction techniques.

### Example Discussion

Adaptive sampling adjusts the sampling rate according to signal dynamics, energy state, or application requirements. Data reduction techniques can reduce communication overhead and processing cost by transmitting fewer samples, compressed measurements, or extracted features.

### Differentiation

Reducing the amount of sensing data is not sufficient by itself. If data reduction is performed without considering task performance, the remaining data may not be sufficient for the target task. CL-TMC is broader because it connects sensing reduction with task-level feedback and controls sensing operations according to task requirements.

### Candidate References

- Adaptive sampling in wireless sensor networks
- Sampling rate control for IoT devices
- Compressed sensing for sensor data acquisition
- Feature reporting and edge inference
- Data reduction for energy-efficient sensing

---

## 5. Redundancy-Aware Sensing and Data Collection

### Role in This Article

These works are used to explain that prior studies have considered redundancy among sensors or data streams.

### Expected Use

Use these references to support the discussion that unnecessary sensing can occur when multiple sensors collect redundant or highly correlated data.

### Example Discussion

Redundancy-aware sensing attempts to reduce duplicate observations by selecting representative sensors, suppressing redundant transmissions, or exploiting spatial/temporal correlation. These techniques are useful for reducing energy and communication overhead.

### Differentiation

Redundancy-aware sensing usually focuses on correlation, coverage, or data similarity. CL-TMC instead focuses on whether each sensing source contributes to the target task performance. Even if two sensing sources are statistically different, one may be unnecessary for a specific task under current conditions. Conversely, apparently redundant data may be useful when uncertainty is high.

### Candidate References

- Redundancy-aware data collection in WSNs
- Correlation-aware sensing
- Representative sensor selection
- Spatial-temporal correlation-based data reduction

---

## 6. Network-Assisted Localization

### Role in This Article

These works are used for the primary use case: energy-efficient localization.

### Expected Use

Use these references in the Introduction and Use Case section to explain how localization can exploit heterogeneous sensing modalities and network-side information.

### Example Discussion

Localization may use GNSS, cellular signals, Wi-Fi, BLE, IMU, and environmental sensing. Different modalities are useful in different environments. For example, GNSS is useful outdoors but limited indoors, while Wi-Fi and BLE can be useful for indoor localization. Cellular and network-side measurements can provide additional positioning information and system context.

### Differentiation

Existing localization studies often focus on improving positioning accuracy using multiple signals or better algorithms. CL-TMC focuses on controlling sensing actions for localization, such as which modalities to activate and how frequently to sense, in order to balance localization accuracy, energy consumption, and communication overhead.

### Candidate References

- Network-assisted localization
- GNSS/Wi-Fi/BLE/IMU-based localization
- Indoor localization using wireless signals
- Multi-modal localization
- Energy-efficient localization

---

## 7. Multi-Channel Biomedical Sensing

### Role in This Article

These works are used for the second representative use case: multi-channel biomedical prediction.

### Expected Use

Use these references to show that biomedical prediction tasks may rely on multiple physiological channels or signals, such as multi-channel ECG, EEG, or other wearable sensing data.

### Example Discussion

In multi-channel ECG systems, different channels may capture different cardiac signal characteristics. However, continuously collecting all channels can increase energy consumption, communication overhead, and processing cost. A task-aware controller can select a subset of channels or adjust sampling rates according to prediction confidence, uncertainty, signal quality, and device constraints.

### Differentiation

Existing biomedical sensing studies often focus on prediction accuracy, signal classification, or channel selection for a fixed dataset. CL-TMC treats multi-channel biomedical sensing as a domain-specific extension of multi-modal sensing and focuses on closed-loop sensing control based on task-level feedback.

### Candidate References

- Multi-channel ECG classification or prediction
- Channel selection for ECG or EEG
- Wearable biomedical sensing
- Energy-efficient health monitoring
- Physiological signal quality-aware sensing

---

## 8. Learning-Based and Optimization-Based Control

### Role in This Article

These works are used in the Open Research Issues section, especially in the subsection on methodology selection.

### Expected Use

Use these references to explain that CL-TMC can be implemented using different control methodologies depending on the system model, task dynamics, complexity, and deployment constraints.

### Example Discussion

Reinforcement learning can be useful because task-aware sensing control is a sequential decision-making problem under uncertainty. Contextual bandits and online learning can provide lower-complexity alternatives when long-term planning is less important. Optimization-based methods can provide interpretable decisions when a reliable system model is available. Rule-based or threshold-based methods can be practical for low-complexity devices.

### Differentiation

The article should not present reinforcement learning as the only solution. Learning-based control is one possible implementation of CL-TMC. The key research issue is how to select an appropriate methodology by considering task requirements, model availability, online/offline operation, computational complexity, safety, and generalization.

### Candidate References

- Reinforcement learning for adaptive sensing
- Contextual bandits for online decision making
- Model predictive control
- Optimization-based sensor selection
- Rule-based or threshold-based sensing control
- Online learning for IoT control

---

## 9. Edge Intelligence and Network-Assisted Feedback

### Role in This Article

These works are used to support the discussion that CL-TMC may require edge/cloud processing and network-side information.

### Expected Use

Use these references in the framework and open research issues sections to explain that the task processor and sensing controller may be deployed at the edge, cloud, device, or network-side control entity.

### Example Discussion

Edge intelligence can support low-latency task inference and sensing control. Network-side information such as channel quality, delay, congestion, resource availability, and transmission cost can help the controller determine whether additional sensing data should be collected or transmitted.

### Differentiation

Existing edge intelligence studies often focus on computation offloading or distributed inference. CL-TMC focuses on using task-level and network-side feedback to control future sensing operations.

### Candidate References

- Edge intelligence for IoT
- Network data analytics
- Cross-layer sensing and communication
- Computation offloading for sensor data processing
- Network-assisted feedback control


---

## Summary of Positioning

The related work should be positioned as follows.

Existing studies have addressed important aspects of sensing and data collection, including multi-modal sensing, energy-efficient sensing, sleep scheduling, adaptive sampling, compressed sensing, redundancy-aware data collection, localization, biomedical sensing, and learning-based control.

However, many existing approaches primarily focus on one of the following objectives:

1. Improving sensing or inference accuracy.
2. Reducing sensing energy.
3. Reducing communication overhead.
4. Reducing redundant data collection.
5. Optimizing sensor/network-level performance.

CL-TMC is different because it focuses on closed-loop task-aware sensing control. The central question is not simply how to collect, compress, or transmit sensing data, but which sensing data are necessary to satisfy the target task requirement under current system conditions.

The article should therefore position CL-TMC as an extension from sensor/network-level efficiency toward task-performance-feedback-based sensing control.