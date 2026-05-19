# III. Closed-Loop Framework for Task-Aware Multi-Modal Sensing Control (Skeleton)

## III-A. CL-TMC Objective and Design Perspective

CL-TMC aims to satisfy task requirements with the minimum necessary sensing, communication, and processing cost under dynamic conditions. The key design perspective is cross-layer: sensing, communication, and task inference are jointly coordinated through feedback.

**Citation needs:** [REF NEEDED: cross-layer adaptive sensing-control frameworks].

## Figure 1 Placeholder

**[Figure 1 about here: CL-TMC architecture]**

**Caption skeleton:** End-to-end CL-TMC architecture linking multi-modal sensing, network context, task processing, and feedback-driven sensing control.

**Message-oriented explanation skeleton:** Figure 1 should make explicit that the feedback path from task-level outcomes to sensing actions is the central differentiator of CL-TMC.

## III-B. Functional Architecture Components

### 1) Multi-Modal Sensing Layer

This layer includes heterogeneous sensing sources (e.g., RF/wireless signals, inertial sensors, vision, environmental sensors, and physiological sensors). It produces candidate observations with different cost and reliability profiles.
Domain-specific multi-channel sensing, such as multi-channel physiological sensing, is treated as a special case of multi-modal sensing in which the controllable sensing units are channels rather than heterogeneous sensor types.

**Citation needs:** [REF NEEDED: heterogeneous sensing modalities in IoT tasks].

### 2) Network and Communication Layer

This layer transports sensing outputs and provides system-side context (e.g., channel quality, delay, congestion, resource availability, transmission cost) used by the controller.

**Citation needs:** [REF NEEDED: network-aware sensing/edge communication context].

### 3) Task Processor

The task processor performs target inference or decision tasks (e.g., localization, prediction, context recognition) and estimates task-level indicators (accuracy/error/confidence/uncertainty/QoE).

**Citation needs:** [REF NEEDED: task-level performance metrics in sensing-driven systems].

### 4) Task-Aware Sensing Controller with Feedback

The controller ingests task indicators and system constraints, then outputs sensing actions for subsequent intervals. This closes the loop between outcomes and future sensing behavior.

**Citation needs:** [REF NEEDED: feedback-driven adaptive sensing control].

## III-C. Core Control Dimensions

- **Modality/channel selection:** choose which sensing sources/channels to activate.
- **Sensing frequency and sampling control:** adjust when and how often to sense.
- **Data representation/reduction control:** choose raw samples, selected samples, compact representations, extracted features, or task-relevant metadata as appropriate.
- **Communication-aware transmission control:** adapt upload strategy under network constraints.
- **Task-performance-aware adaptation:** increase/decrease sensing intensity based on uncertainty, error, or QoE.

Compressed sensing can be considered one optional data reduction mechanism in this dimension set; CL-TMC is not restricted to compressed sensing.

**Citation needs:** [REF NEEDED: modality selection], [REF NEEDED: adaptive sampling], [REF NEEDED: communication-aware control], [REF NEEDED: task feedback metrics].

## III-D. Closed-Loop Operation Flow

CL-TMC operates iteratively rather than as a one-shot data collection pipeline. In each control interval, multi-modal sensors first collect data according to the current sensing configuration. The network then delivers sensing data together with system-side context such as delay, channel condition, and resource status.

Next, the task processor performs the target inference task and evaluates task-level indicators (for example, error, uncertainty, confidence, or QoE). Based on these indicators and current system constraints, the sensing controller determines the next sensing configuration, including potential updates to modality selection, sensing frequency, and data representation strategy.

Finally, this feedback decision is applied to future sensing intervals, and the loop repeats. This repeated task-feedback-to-sensing cycle is the central property of CL-TMC and distinguishes it from static or one-shot sensing data collection architectures.

**Citation needs:** [REF NEEDED: iterative closed-loop sensing-control pipelines], [REF NEEDED: task-feedback-driven sensing adaptation over time].

