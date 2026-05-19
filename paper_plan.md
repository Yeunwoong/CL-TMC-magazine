# Paper Plan

## Tentative Title

A Closed-Loop Framework for Task-Aware Multi-Modal Sensing Control

## Paper Type

Magazine-style article.

This article should focus on motivation, architectural framework, representative use cases, enabling technologies, and open research challenges. It should not be written as a transaction-style paper with heavy mathematical formulation or extensive theorem-based analysis.

## Target Paper

IEEE Communications Magazine, IEEE Network, IEEE IoT Magazine, IEEE Wireless Communications.

## Core Message

IoT-based task processing system should not collect and transmit sensing data uniformly. Instead, sensing operations should be dynamically controlled according to the performance requirement of the target application.

The key idea is to use task-level feedback, such as localization accuracy, detection accuracy, prediction error, or service-level QoE, to control multi-modal (or multi-channel) sensing operations in a closed-loop manner.

In this article, multi-modal sensing primarily refers to the use of heterogeneous sensing sources, such as GNSS, cellular, Wi-Fi, BLE, IMU, camera, and environmental sensors. Multi-channel sensing can be regarded as a special case or domain-specific extension of multi-modal sensing, where multiple channels of homogeneous or domain-specific sensors are selectively used for a target task. Therefore, the proposed framework mainly uses the term multi-modal sensing, while also covering multi-channel sensing scenarios.

## Background Motivation

Future IoT-based task processing systems are expected to support sensing-intensive and context-aware applications such as localization, digital twins, XR services, autonomous mobility, and biomedical predicstions. These applications often rely on heterogeneous sensing modalities (or various sensing channels). For example, network-assisted localization task includs cellular signals, Wi-Fi, BLE, IMU, and environmental sensors. As another example, biomedical prediction task includes multiple channel data, which will be aggregated to predict a specific biomedical situation.

However, collecting all available sensing data at a fixed sensing rate can cause excessive energy consumption, uplink traffic, and processing overhead. At the same time, overly aggressive sensing reduction may degrade the performance of the target application.

Therefore, sensing should be controlled based on the actual requirement and performance of the target task.

## Main Problem

Conventional sensing and data collection frameworks are mostly data-centric. They focus on collecting, compressing, or transmitting sensing data, but they do not sufficiently consider how much sensing is actually necessary for the target task.

The missing component is a closed-loop mechanism that connects task performance to sensing control.

## Proposed Framework

The proposed framework consists of the following components.

1. Multi-modal sensor layer (or multi-channel sensor layer) 
   - Collects heterogeneous sensing data from GNSS, cellular, Wi-Fi, BLE, IMU, and other sensors.
   - (or, collects multi-channel sensing data from multiple channels of homogeneous sensors.)

2. Network layer  
   - Delivers sensing data from devices to the task processor.
   - Provides network-side information such as channel condition, delay, congestion, and resource availability.

3. Task processor  
   - Performs application-level tasks such as localization, mobility prediction, environment recognition, digital twin update, or biomedical predictions.
   - Evaluates task-level performance such as accuracy, error, reliability, or QoE.

4. Sensing controller  
   - Determines sensing actions based on task feedback and network/system conditions.
   - Controls modality (or channel) selection, sensing frequency, sampling rate, data reduction level, and transmission strategy.

5. Feedback loop  
   - Feeds task performance back to the sensing controller.
   - Enables adaptive sensing control rather than static sensing policies.

## Main Contributions

First, this article presents a closed-loop framework for task-aware multi-modal sensing control, where sensing operations are dynamically adjusted based on task-level feedback rather than fixed sensing policies.

Second, it identifies key control dimensions of multi-modal (or multi-channel) sensing, including modality (or channel) selection, sensing frequency control, sampling/data reduction, and communication-aware sensing adaptation.

Third, it discusses representative use cases, with a particular focus on energy-efficient localization, to show how task-aware sensing control can reduce unnecessary sensing and communication overhead while maintaining application-level performance. 

Finally, it outlines open research challenges, including task-performance modeling, reinforcement learning-based sensing control, network-assisted feedback design, and practical implementation issues in future IoT systems.

## Primary Use Case

Primary use case is energy-efficient localization.

Localization can use multiple sensing modalities such as GNSS, cellular, Wi-Fi, BLE, IMU, and other sensor measurements. GNSS can provide accurate outdoor positioning but consumes relatively high energy and may not work well indoors. Wi-Fi and BLE can be useful for indoor localization, while cellular measurements can provide network-assisted positioning information.

The sensing controller should select appropriate sensing modalities and sensing frequencies depending on the required localization accuracy, device energy state, network condition, and environment.

For example, when coarse localization is sufficient, low-energy sensing modalities may be used. When high localization accuracy is required, additional modalities or higher sensing frequency can be activated. Reinforcement learning can be used to learn this sensing control policy under unknown and dynamic system conditions.

## Additional Use Cases

Possible additional use cases include:

1. Biomedical predictions
2. Mobility prediction
3. Digital twin update
4. XR/context-aware service support
5. Network-assisted sensing for autonomous systems

## Important Writing Instructions

- Write in a magazine-style tone.
- Avoid heavy mathematical derivations.
- Emphasize architecture, motivation, intuition, and future research directions.
- Do not describe the paper as a compressed sensing-only paper.
- Compressed sensing can be mentioned as one possible data reduction technique, but the framework should be broader.
- Do not invent citations.
- If a citation is required but no reference is available, mark it as [REF NEEDED].
- Clearly distinguish this magazine-style article from a transaction-style localization paper.
- Use "multi-modal sensing" as the main terminology throughout the article.
- Explain that multi-channel sensing can be regarded as a special case or domain-specific extension of multi-modal sensing.
- Do not treat multi-modal sensing and multi-channel sensing as two separate frameworks.