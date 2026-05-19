# Paper Outline

## Title

A Closed-Loop Framework for Task-Aware Multi-Modal Sensing Control

## I. Introduction

### Purpose

Introduce the need for a closed-loop framework for task-aware multi-modal sensing control in future IoT systems.

### Paragraph 1: Sensing-intensive IoT applications

Future IoT systems are expected to support sensing-intensive and context-aware applications. Examples include network-assisted localization, digital twin services, XR/context-aware services, autonomous mobility, smart healthcare, and biomedical prediction. These applications require continuous or periodic sensing from devices, environments, and networks.

### Paragraph 2: Need for heterogeneous sensing data

These applications often require heterogeneous sensing data because a single sensing source cannot fully capture all task-relevant information. Different sensors observe different physical phenomena, provide different feature representations, and exhibit different limitations in terms of accuracy, robustness, energy consumption, coverage, and environmental dependency.

For example, localization may rely on GNSS, cellular measurements, Wi-Fi, BLE, IMU, and environmental sensors. GNSS can provide useful outdoor positioning information, while Wi-Fi, BLE, and IMU can provide complementary information for indoor or GNSS-denied environments. Similarly, biomedical prediction may exploit multiple physiological sensing channels, such as multi-channel ECG signals, where different channels may capture different cardiac signal characteristics.

In this article, multi-modal sensing mainly refers to heterogeneous sensing sources. Multi-channel sensing can be regarded as a special case or domain-specific extension of multi-modal sensing, where multiple channels of homogeneous or domain-specific sensors are selectively used for a target task.

### Paragraph 3: Limitation of static sensing and data collection policies

However, many existing sensing and data collection systems still rely on static or predefined sensing policies. Sensors may collect data at fixed rates, transmit predefined sensing streams, or activate sensing functions without explicitly considering the actual requirement of the target task.

Collecting all sensing data uniformly can cause excessive energy consumption, uplink traffic, and processing overhead. Prior studies have addressed energy-efficient sensing and data collection through techniques such as sleep scheduling, duty cycling, adaptive sampling, and redundancy-aware sensor activation. These approaches are important, but many of them primarily focus on sensor/network-level efficiency rather than explicitly closing the loop between task performance and sensing control.

### Paragraph 4: Proposed direction: CL-TMC

To overcome this limitation, this article proposes a closed-loop framework for task-aware multi-modal sensing control, referred to as CL-TMC.

The key issue is not only how to collect sensing data, but how to determine what sensing data are necessary for the target task. Instead of uniformly collecting all available sensing data, CL-TMC uses task-level feedback, such as localization accuracy, prediction error, detection confidence, or service-level QoE, to control sensing operations. A closed-loop framework is therefore needed to connect task performance with sensing control.

### Paragraph 5: Key contributions

The key contributions of this article are summarized as follows.

First, we present CL-TMC, a closed-loop framework that connects task-level performance feedback with multi-modal sensing control.

Second, we identify key control dimensions of task-aware sensing, including modality selection, channel selection, sensing frequency control, sampling rate control, and network-aware transmission control.

Third, we discuss representative use cases, including energy-efficient localization and multi-channel biomedical prediction, to show how CL-TMC can reduce unnecessary sensing and communication overhead while maintaining task-level performance.

Finally, we discuss open research issues for realizing CL-TMC, including task-performance modeling, methodology selection, dataset construction, scalable implementation, network-assisted feedback, and privacy-aware deployment.

### Paragraph 6: Organization

The remainder of this article is organized as follows. Section II explains the transition from data-centric data collection to task-aware sensing control. Section III presents the proposed CL-TMC framework, including its functional components and control dimensions. Section IV discusses representative use cases of CL-TMC, including energy-efficient localization and multi-channel biomedical prediction. Section V presents open research issues for realizing CL-TMC in practical IoT and wireless systems. Finally, Section VI concludes the article.
---

## II. From Data-Centric Data Collection to Task-Aware Sensing Control

### Purpose

Explain how existing sensing and data collection approaches have evolved, and clarify why task-aware closed-loop sensing control is needed.

### A. Static and Periodic Sensing

Many IoT sensing systems rely on static or periodic sensing policies. Sensors collect data using predefined sensing modalities, sampling rates, and reporting intervals. This approach is simple and reliable, but it cannot adapt to changes in task requirements, user context, device energy state, network condition, or environmental dynamics.

### B. Energy-Efficient Sensing and Data Collection

Prior studies have investigated energy-efficient sensing and data collection techniques such as sleep scheduling, duty cycling, sensor activation control, redundancy-aware data collection, and energy-aware routing. These approaches can reduce sensing energy and extend network lifetime. However, they mainly focus on sensor-level or network-level efficiency metrics, such as energy consumption, coverage, connectivity, and data collection cost.

### C. Data Reduction and Adaptive Sampling

Another line of work focuses on reducing the amount of sensing data through adaptive sampling, sampling rate control, selective data acquisition, feature reporting, or sparsity-aware data acquisition.

Compressed sensing can be considered one possible data reduction technique, but CL-TMC is broader than compressed sensing because it controls sensing operations based on task-level feedback.

### D. Toward Task-Aware Closed-Loop Control

The above approaches are important, but they do not fully close the loop between task performance and sensing control. In task-aware sensing control, the objective is not simply to maximize data collection or minimize sensing cost. Instead, the objective is to satisfy the target task requirement with minimum necessary sensing, communication, and computation cost.

Therefore, the key question should be shifted from “How can we collect or reduce sensing data?” to “Which sensing data are necessary to satisfy the target task requirement under system constraints?” This motivates the proposed CL-TMC framework, where task-level feedback is used to dynamically control sensing operations.

---

## III. Closed-Loop Framework for Task-Aware Multi-Modal Sensing Control

### Purpose

Present the overall CL-TMC framework and explain how task-level feedback is used to control multi-modal sensing operations.

### A. Overall Architecture of CL-TMC

The proposed CL-TMC framework consists of four major functional blocks: multi-modal sensing layer, network/communication layer, task processor, and task-aware sensing control and feedback. Multi-modal sensors collect heterogeneous sensing data, the network delivers sensing data and provides system-side information, the task processor performs the target application and evaluates task-level performance, and the sensing control loop adapts future sensing operations based on task feedback.

The key idea of CL-TMC is to close the loop between task processing and sensing operation. Instead of collecting all available sensing data using fixed policies, CL-TMC determines what sensing data are necessary for the target task under current device, network, and environmental conditions.

### B. Functional Components

The multi-modal sensing layer collects heterogeneous sensing data from wireless signals, vision sensors, inertial sensors, environmental sensors, physiological sensors, and other domain-specific sensors. In this article, multi-modal sensing mainly refers to heterogeneous sensing sources, while multi-channel sensing is regarded as a special case or domain-specific extension of multi-modal sensing.

The network and communication layer delivers sensing data from devices to the task processor. It can also provide network-side information, such as channel quality, delay, congestion level, resource availability, and transmission cost. This information is important because sensing control should consider not only task performance but also communication overhead and network conditions.

The task processor performs application-level tasks such as localization, mobility prediction, biomedical prediction, digital twin update, and context-aware service support. It may include preprocessing, feature extraction, multi-modal fusion, filtering, optimization, and AI/ML/DL-based inference. The output of the task processor is not limited to the final task result, but may also include task-level performance indicators such as accuracy, uncertainty, confidence score, prediction error, reliability, or QoE.

The task-aware sensing control and feedback block determines future sensing actions based on task-level feedback and system conditions. It closes the gap between task processing and sensing operation by allowing the system to adapt future sensing behavior according to the actual requirement of the target task.

### C. Control Dimensions

CL-TMC can control sensing operations along multiple dimensions. First, modality or channel selection determines which sensing sources should be activated for the current task. For example, localization may use GNSS, cellular, Wi-Fi, BLE, and IMU measurements, while biomedical prediction may use selected channels from multi-channel physiological signals.

Second, sensing rate and sampling control determine how frequently each sensing source should collect data. Higher sensing rates may improve task performance under dynamic conditions, but they also increase energy consumption, communication overhead, and processing cost.

Third, data representation and reduction determine whether the system should transmit raw sensing data, selected samples, compressed measurements, extracted features, or task-relevant metadata. This dimension includes adaptive sampling and compressed sensing as possible techniques, but CL-TMC is broader than any single data reduction method.

Fourth, communication-aware transmission control determines how sensing data should be delivered under network constraints. The sensing controller may consider channel quality, delay, congestion, resource availability, and uplink transmission cost.

Finally, task-performance-aware adaptation determines how sensing actions should change according to task-level feedback. For example, if localization uncertainty is low, the controller may reduce sensing frequency or deactivate high-energy modalities. If prediction confidence decreases, the controller may activate additional sensing channels or increase the sampling rate.

### Expected Message

CL-TMC is not only a sensing data collection framework, but a closed-loop control framework that determines which sensing data are necessary, when they should be collected, and how they should be delivered based on task-level feedback and system conditions.

---

## IV. Use Cases of CL-TMC

### Purpose

Demonstrate how the proposed CL-TMC framework can be applied to representative sensing-intensive IoT applications.

### A. Energy-Efficient Localization

Localization is a representative task that can benefit from task-aware multi-modal sensing control. A device may use multiple sensing modalities, such as GNSS, cellular measurements, Wi-Fi, BLE, IMU, and environmental sensors. However, activating all modalities at a high sensing rate can cause excessive energy consumption and communication overhead.

In CL-TMC, the sensing controller can select appropriate sensing modalities and sensing rates according to localization accuracy requirements, device energy state, environmental conditions, and network status. For example, when coarse localization is sufficient or localization uncertainty is low, the controller may rely on low-energy modalities or reduce sensing frequency. When high accuracy is required or uncertainty increases, additional modalities can be activated.

A learning-based controller can be used as one possible implementation, but the key message of this use case is not the superiority of a specific learning algorithm. Rather, the goal is to show how closed-loop task-aware sensing control can reduce sensing overhead while maintaining localization performance.

### B. Multi-Channel Biomedical Prediction

Biomedical prediction is another representative use case, where multiple physiological sensing channels may be available. For example, a multi-channel ECG system can collect signals from multiple channels, and different channels may capture different cardiac signal characteristics. However, continuously collecting all channels may increase device energy consumption, communication overhead, and processing cost.

In CL-TMC, multi-channel biomedical sensing can be regarded as a domain-specific extension of multi-modal sensing. The sensing controller can determine which physiological channels should be activated and how frequently they should be sampled according to prediction confidence, uncertainty, patient condition, and device energy state.

For example, if the prediction confidence is high, the system may use a reduced set of channels or lower sampling frequency. If the prediction confidence decreases or abnormal patterns are detected, additional channels or higher sampling rates can be activated. This illustrates how CL-TMC can adapt sensing operations based on task-level feedback rather than fixed channel selection.

### Expected Message

CL-TMC is a general framework that can support both heterogeneous multi-modal sensing scenarios and domain-specific multi-channel sensing scenarios.

---

## V. Open Research Issues

### Purpose

Discuss key research challenges that should be addressed to realize CL-TMC in practical IoT and wireless systems.

### A. Task-Performance Modeling

A fundamental challenge is to model the relationship between sensing actions and task performance. CL-TMC requires the sensing controller to determine which sensing data are necessary for the target task. However, the impact of modality selection, channel selection, sensing frequency, sampling rate, and data representation on task accuracy, uncertainty, confidence, or QoE is often nonlinear and environment-dependent.

For example, in localization, the contribution of GNSS, Wi-Fi, BLE, cellular, and IMU measurements may vary depending on indoor/outdoor conditions, mobility, blockage, and network status. In biomedical prediction, the importance of each physiological channel may vary depending on patient condition, signal quality, and target prediction task. Therefore, task-performance modeling is required to connect sensing decisions with task-level outcomes.

### B. Methodology Selection for Task-Aware Sensing Control

Another important issue is how to select an appropriate control methodology for CL-TMC. Since task-aware sensing control involves sequential decision making under uncertainty, learning-based methods such as reinforcement learning, contextual bandits, and online learning can be useful. These methods can adapt sensing policies based on task feedback without requiring a complete analytical model of the system.

However, learning-based methods may require training data, exploration, computational resources, and careful safety management. Their convergence and generalization can also be challenging in dynamic IoT environments.

Non-learning-based methods can also be considered. Rule-based control is simple and easy to implement, but may not adapt well to complex environments. Optimization-based methods can provide interpretable decisions when the system model is available, but they may suffer from high computational complexity or limited applicability under unknown dynamics. Model predictive control can support online adaptation, but requires predictive models and repeated optimization. Heuristic or threshold-based methods may be practical for low-complexity devices, but their performance may be scenario-dependent.

Therefore, the methodology should be selected by jointly considering task requirements, system dynamics, model availability, computational complexity, online/offline operation, and deployment constraints. In this article, learning-based control is regarded as one possible implementation of CL-TMC, not as the only solution.

### C. Dataset and Evaluation Methodology

Evaluating CL-TMC requires datasets that include not only raw sensing data but also task-level labels, system states, and sensing cost information. For example, localization datasets should include multi-modal sensing measurements, ground-truth positions, energy consumption, and network conditions. Biomedical datasets should include multi-channel physiological signals, prediction labels, signal quality indicators, and acquisition costs.

Without such datasets, it is difficult to evaluate whether sensing reduction truly preserves task performance. Therefore, benchmark datasets and evaluation metrics are required to compare different sensing control policies fairly.

### D. Real-Time and Scalable Implementation

CL-TMC should operate under practical latency, energy, and computational constraints. The sensing controller may need to make decisions in real time, especially for mobility, XR, healthcare, and autonomous systems. However, as the number of sensors, channels, devices, and tasks increases, the control space becomes large.

Scalable implementation requires lightweight decision algorithms, hierarchical control, edge-assisted processing, and possibly offline-trained policies with online adaptation. The tradeoff between control optimality and implementation complexity should be carefully considered.

### E. Network-Assisted Feedback and Cross-Layer Design

The network can provide important information for sensing control, including channel quality, delay, congestion, resource availability, and transmission cost. However, how to expose such network-side information to the sensing controller remains an open issue.

A cross-layer design is needed to connect sensing, communication, computation, and task processing. For example, a sensing decision may reduce device energy consumption but increase task uncertainty; a transmission decision may reduce uplink overhead but increase inference delay. CL-TMC should therefore jointly consider sensing cost, communication cost, computation cost, and task performance.

### F. Privacy, Security, and Standardization Issues

Multi-modal sensing data may include privacy-sensitive information, such as location, visual data, physiological signals, and behavior patterns. Therefore, CL-TMC should consider privacy-preserving sensing, secure feedback, access control, and trustworthy task inference.

In addition, practical deployment may require standardized interfaces between sensors, network entities, edge/cloud processors, and task-aware sensing controllers. Without such interfaces, it may be difficult to deploy closed-loop sensing control across heterogeneous IoT and wireless systems.

### Expected Message

CL-TMC opens several research issues beyond algorithm design. Practical realization requires task-performance modeling, appropriate methodology selection, dataset construction, scalable implementation, network-assisted feedback, and privacy-aware deployment.

---

## VI. Conclusion

### Purpose
Summarize the article.

### Expected Message
Future sensing-intensive systems should move from static, data-centric sensing to adaptive, task-aware, and closed-loop sensing control.