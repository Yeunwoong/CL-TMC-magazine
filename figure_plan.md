# Figure Plan

## Overall Figure Strategy

This magazine-style article will use four main figures.

1. A conceptual framework figure for the proposed closed-loop framework for task-aware multi-modal sensing control (CL-TMC).
2. A combined use-case architecture figure with two subfigures:
   - Figure 2(a): Energy-efficient localization
   - Figure 2(b): Multi-channel biomedical prediction
3. A performance figure for Use Case 1: energy-efficient localization.
4. A performance figure for Use Case 2: multi-channel biomedical prediction.

The figures should support the main narrative of the article:

- Figure 1 explains what CL-TMC is.
- Figure 2 explains how CL-TMC can be instantiated in representative applications.
- Figure 3 shows why CL-TMC is useful for localization.
- Figure 4 shows why CL-TMC is useful for multi-channel biomedical prediction.

Because this is a magazine-style article, all figures should be visually intuitive, message-oriented, and not overly detailed. The goal is to communicate architectural insights and performance tradeoffs rather than algorithmic details.

---

## Figure 1. Closed-Loop Framework for Task-Aware Multi-Modal Sensing Control

### Purpose

Present the overall CL-TMC architecture and illustrate the closed-loop relationship among sensing, communication, task processing, and task-aware sensing control.

### Main Components

#### 1. Multi-Modal Sensing Layer

The figure should use general sensing categories rather than use-case-specific sensor names.

Recommended categories:

- Wireless / RF signals
- Vision sensors
- Inertial sensors
- Environmental sensors
- Physiological sensors
- Others

The purpose is to show that CL-TMC can support heterogeneous sensing sources across different IoT and wireless applications.

#### 2. Network / Communication Layer

This block delivers sensing data from sensors or devices to the task processor.

It may also provide network-side information, such as:

- Channel quality
- Delay
- Congestion level
- Resource availability
- Transmission cost

This block should make it clear that the network is not only a data pipe, but can also provide useful system-side information for sensing control.

#### 3. Task Processor

The task processor performs application-level inference using sensing data.

It may include:

- Preprocessing
- Feature extraction
- Multi-modal fusion
- Filtering
- Optimization
- ML/DL-based inference
- Task inference

Recommended wording inside the figure:

- "Task Intelligence"
- "ML/DL, Optimization, Filtering, and Inference Models"

The task processor output may include:

- Task result
- Accuracy
- Uncertainty
- Confidence score
- Prediction error
- Reliability
- QoE

#### 4. Task-Aware Sensing Control and Feedback

This block receives task-level feedback and system-side information, and determines future sensing actions.

Recommended control dimensions:

- Modality / channel selection
- Sensing rate and sampling control
- Data reduction / feature reporting
- Power and duty-cycle management

The feedback arrow should clearly connect the task processor or sensing controller back to the sensing layer.

### Key Message

CL-TMC closes the loop between task performance and sensing operation. Instead of collecting all available sensing data using fixed policies, CL-TMC determines what sensing data are necessary, when they should be collected, and how they should be delivered according to task-level feedback and system conditions.

### Design Notes

- The figure should be general rather than localization-specific.
- Avoid making the sensor examples too focused on radar, camera, Wi-Fi, or robotics.
- Use broad sensing categories to cover both heterogeneous multi-modal sensing and domain-specific multi-channel sensing.
- The feedback block should emphasize control dimensions rather than low-level examples such as beam steering or specific sensor parameters.
- The closed-loop path should be visually emphasized.
- Avoid algorithm-specific labels such as "DQN" or "RL agent" in this figure.

### Candidate Caption

**Figure 1.** Closed-loop framework for task-aware multi-modal sensing control (CL-TMC). Multi-modal sensing data are delivered through the network to the task processor, which evaluates task-level performance and feeds back control decisions to adapt future sensing operations.

### Candidate Main-Text Reference

Fig. 1 illustrates the overall CL-TMC architecture. The framework connects multi-modal sensing, network-assisted data delivery, task processing, and task-aware sensing control through a closed feedback loop. The key principle is to use task-level feedback to determine which sensing data are necessary under current system conditions.

---

## Figure 2. Representative Use Cases of CL-TMC

### Purpose

Show how the proposed CL-TMC framework can be instantiated in two representative application scenarios.

- Figure 2(a): Energy-efficient localization
- Figure 2(b): Multi-channel biomedical prediction

The purpose of this figure is to show that CL-TMC is not limited to one application domain. It can support both heterogeneous multi-modal sensing scenarios and domain-specific multi-channel sensing scenarios.

---

## Figure 2(a). Use Case 1: Energy-Efficient Localization

### Components

Recommended components:

1. Device / user / robot
2. Sensing sources
   - GNSS
   - Cellular
   - Wi-Fi
   - BLE
   - IMU
   - Environmental sensors
3. Network / edge server
4. Localization processor
5. Localization performance evaluator
   - Position estimate
   - Localization error
   - Uncertainty
6. Sensing controller
7. Feedback to sensing modules

### Data and Control Flow

- The device collects sensing data from multiple localization-related modalities.
- Sensing data are transmitted to a localization processor through the network.
- The localization processor estimates the position and evaluates localization quality.
- The sensing controller uses localization feedback and system conditions to adjust future sensing actions.
- Control decisions are fed back to the device or sensing modules.

### Key Message

Different sensing modalities contribute differently depending on environment, mobility, and required localization accuracy. CL-TMC adaptively selects sensing modalities and sensing rates to reduce sensing cost while maintaining localization performance.

### Design Notes

- Do not make this figure too algorithm-specific.
- The controller can be described as "task-aware sensing controller" rather than "RL agent."
- The figure should emphasize the tradeoff between localization accuracy and sensing/communication cost.
- The figure should be consistent with the general framework in Fig. 1.

---

## Figure 2(b). Use Case 2: Multi-Channel Biomedical Prediction

### Components

Recommended components:

1. Wearable / biomedical sensing device
2. Multi-channel physiological sensing
   - ECG channels
   - Optional physiological channels if needed
3. Network / edge / cloud processor
4. Biomedical prediction engine
5. Prediction performance evaluator
   - Prediction label
   - Confidence
   - Uncertainty
   - Prediction error
6. Sensing controller
7. Feedback to channel selection and sampling control

### Data and Control Flow

- The biomedical device collects physiological signals from multiple channels.
- The collected signals or features are transmitted to the prediction engine.
- The prediction engine performs the target biomedical prediction task.
- Prediction confidence, uncertainty, or error is evaluated.
- The sensing controller determines which channels should be activated and how frequently they should be sampled.
- Control decisions are fed back to the biomedical sensing device.

### Key Message

Different physiological channels may contribute differently to the target prediction task. CL-TMC adaptively selects sensing channels and sampling rates according to prediction confidence, uncertainty, and device constraints.

### Design Notes

- This use case should be presented as a domain-specific extension of multi-modal sensing.
- The figure should clearly show that multi-channel sensing is treated as a special case of CL-TMC.
- Avoid excessive medical detail unless directly needed for the target prediction task.
- The figure should emphasize channel selection, sampling control, and task-level feedback.

### Overall Message of Figure 2

CL-TMC can support both heterogeneous multi-modal sensing scenarios and domain-specific multi-channel sensing scenarios.

### Candidate Caption

**Figure 2.** Representative use cases of CL-TMC: (a) energy-efficient localization using heterogeneous sensing modalities and (b) multi-channel biomedical prediction using adaptive channel selection and sampling control.

### Candidate Main-Text Reference

Fig. 2 shows two representative instantiations of CL-TMC. In energy-efficient localization, the controller adjusts localization-related sensing modalities such as GNSS, cellular, Wi-Fi, BLE, and IMU. In multi-channel biomedical prediction, the controller selects physiological sensing channels and sampling rates according to prediction feedback.

---

## Figure 3. Performance Evaluation for Use Case 1: Energy-Efficient Localization

### Purpose

Provide quantitative evidence that task-aware sensing control can improve the tradeoff between localization performance and sensing or communication cost.

### Recommended Figure Structure

Use one figure with one or two subfigures.

Recommended structure:

- Figure 3(a): Localization performance versus sensing cost
- Figure 3(b): Energy saving or active sensing modalities under different accuracy requirements

If space is limited, use only one main tradeoff plot.

### Candidate Plot Option A: Localization Error vs. Sensing Energy

- x-axis: Average sensing energy consumption
- y-axis: Localization error
- curves:
  - CL-TMC
  - Always-on sensing
  - Fixed periodic sensing
  - Reduced sensing baseline
  - Heuristic adaptive sensing baseline

Main message:

CL-TMC achieves a better localization error-energy tradeoff than static sensing baselines.

### Candidate Plot Option B: Required Sensing Cost vs. Target Accuracy

- x-axis: Target localization accuracy requirement
- y-axis: Required sensing cost or energy consumption
- curves:
  - CL-TMC
  - Static sensing baseline
  - Heuristic adaptive sensing baseline

Main message:

CL-TMC adapts sensing effort according to the required localization accuracy.

### Candidate Plot Option C: Active Modalities Over Time

- x-axis: Time, episode, or scenario index
- y-axis: Number of active sensing modalities
- optional additional plot or inset:
  - Localization error
  - Localization uncertainty

Main message:

CL-TMC dynamically changes sensing behavior according to task feedback.

### Preferred Main Message

CL-TMC can reduce sensing energy and/or communication overhead while maintaining the required localization accuracy.

### Design Notes

- Avoid too many curves.
- Use the performance plot to emphasize closed-loop adaptation, not the superiority of a specific learning algorithm.
- Do not label the proposed method as "DQN" or "RL" in the main figure unless necessary.
- If the underlying implementation is learning-based, describe it in the text as one possible implementation of CL-TMC.
- The comparison should include at least one static or always-on baseline.

### Candidate Caption

**Figure 3.** Performance evaluation for energy-efficient localization. CL-TMC improves the tradeoff between localization performance and sensing cost by adaptively controlling sensing modalities and sensing rates according to task feedback.

### Candidate Main-Text Reference

Fig. 3 illustrates the benefit of task-aware sensing control in the localization use case. The key observation is that closed-loop adaptation can reduce sensing cost while satisfying localization performance requirements.

---

## Figure 4. Performance Evaluation for Use Case 2: Multi-Channel Biomedical Prediction

### Purpose

Show that CL-TMC can reduce sensing and processing overhead in multi-channel biomedical prediction while preserving task-level prediction performance.

### Recommended Figure Structure

Use one figure with one or two subfigures.

Recommended structure:

- Figure 4(a): Prediction performance versus number of active channels or sensing cost
- Figure 4(b): Average active channels or energy consumption under different confidence/uncertainty requirements

If space is limited, use only one main tradeoff plot.

### Candidate Plot Option A: Prediction Performance vs. Active Channels

- x-axis: Number of active sensing channels or sensing cost
- y-axis: Prediction accuracy, F1-score, or AUROC
- curves:
  - CL-TMC
  - All-channel sensing
  - Fixed reduced-channel baseline
  - Heuristic channel selection baseline

Main message:

CL-TMC preserves prediction performance while using fewer sensing channels.

### Candidate Plot Option B: Active Channels vs. Confidence Requirement

- x-axis: Confidence threshold or target performance requirement
- y-axis: Average number of active channels or energy consumption
- curves:
  - CL-TMC
  - Static full-channel baseline
  - Static reduced-channel baseline

Main message:

CL-TMC adapts sensing effort according to prediction confidence requirements.

### Candidate Plot Option C: Robustness Under Signal Quality Variations

- x-axis: Noise level, missing-channel ratio, or signal quality condition
- y-axis: Prediction performance
- curves:
  - CL-TMC
  - All-channel sensing
  - Fixed reduced-channel sensing

Main message:

CL-TMC can adapt channel usage under varying signal quality or uncertainty.

### Preferred Main Message

CL-TMC can use fewer sensing channels or lower sensing effort while preserving biomedical prediction performance.

### Design Notes

- Choose the evaluation metric that best matches the biomedical task.
- For classification, use accuracy, F1-score, or AUROC.
- For prediction or regression, use MAE, RMSE, or another suitable error metric.
- If possible, report both task performance and sensing efficiency.
- Keep visual style consistent with Figure 3.
- Avoid making the figure look like a purely biomedical algorithm comparison; the focus should remain on sensing control.

### Candidate Caption

**Figure 4.** Performance evaluation for multi-channel biomedical prediction. CL-TMC reduces sensing effort through adaptive channel selection and sampling control while preserving task-level prediction performance.

### Candidate Main-Text Reference

Fig. 4 shows the effectiveness of CL-TMC in a domain-specific multi-channel sensing scenario. By using task-level prediction feedback, CL-TMC can reduce the number of active physiological sensing channels or the sensing effort while maintaining prediction performance.

---

## Cross-Figure Design Guidelines

### 1. Consistent Terminology

Use the same terminology across all figures:

- CL-TMC
- Multi-modal sensing
- Multi-channel sensing
- Task processor
- Task-level feedback
- Sensing controller
- Sensing modality / sensing channel
- Sensing cost
- Task performance

### 2. Consistent Visual Logic

The figures should follow a consistent visual logic:

- Framework figures should emphasize information flow and feedback loops.
- Use-case figures should show how the same framework is instantiated in different domains.
- Performance figures should emphasize tradeoffs between task performance and sensing cost.

### 3. Message-Oriented Figure Design

Each figure should communicate one primary message:

- Figure 1: What CL-TMC is
- Figure 2: Where CL-TMC can be applied
- Figure 3: Why CL-TMC helps in localization
- Figure 4: Why CL-TMC helps in biomedical prediction

### 4. Avoid Overly Detailed Diagrams

Because this is a magazine-style article, figures should be intuitive and visually clean.

Avoid:

- Too many arrows
- Too many low-level parameters
- Algorithm-specific labels
- Excessive mathematical notation
- Too many baselines in performance plots

### 5. Keep RL as an Implementation Option

If the performance results are generated using a reinforcement learning-based controller, describe RL as one possible implementation of CL-TMC.

The main message of the figures should not be:

"RL outperforms baselines."

The main message should be:

"Closed-loop task-aware sensing control reduces sensing cost while preserving task-level performance."

### 6. Flexibility

If the final paper length becomes tight:

- Figure 3 and Figure 4 can each be simplified into a single plot.
- If necessary, Figure 3 and Figure 4 can be combined into one performance comparison figure with two subfigures.
- Figure 2 should remain a combined use-case figure because it helps communicate the generality of CL-TMC.

---

## Final Figure List

- **Figure 1.** Closed-loop framework for task-aware multi-modal sensing control.
- **Figure 2.** Representative use cases of CL-TMC: (a) energy-efficient localization and (b) multi-channel biomedical prediction.
- **Figure 3.** Performance evaluation for energy-efficient localization.
- **Figure 4.** Performance evaluation for multi-channel biomedical prediction.