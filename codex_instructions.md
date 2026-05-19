# Codex Instructions

## Project

This project is for drafting a magazine-style article titled:

**A Closed-Loop Framework for Task-Aware Multi-Modal Sensing Control**

The article proposes CL-TMC, a closed-loop framework that connects task-level performance feedback with multi-modal sensing control.

## Target Style

The article should be written in a magazine-style tone, suitable for venues such as IEEE Communications Magazine, IEEE Network, IEEE IoT Magazine, or IEEE Wireless Communications.

The writing should emphasize:

- Motivation
- Architectural framework
- Intuitive explanation
- Representative use cases
- Open research issues
- Practical insights

The writing should avoid:

- Heavy mathematical derivations
- Theorem-style presentation
- Overly detailed algorithmic formulation
- Transaction-style technical depth
- Excessive emphasis on one specific algorithm

## Files to Read First

Before drafting any section, read the following files:

1. `paper_plan.md`
2. `outline.md`
3. `figure_plan.md`
4. `related_work_notes.md`
5. `references.bib`, if available

## Main Concept

The key idea of CL-TMC is that sensing operations should be controlled based on the actual requirement and performance of the target task.

The central question is not simply:

> How can we collect, compress, or transmit sensing data?

Instead, the central question is:

> Which sensing data are necessary to satisfy the target task requirement under current system conditions?

## Terminology

Use **multi-modal sensing** as the main terminology throughout the article.

Multi-modal sensing mainly refers to heterogeneous sensing sources, such as wireless/RF signals, vision sensors, inertial sensors, environmental sensors, and physiological sensors.

Multi-channel sensing can be regarded as a special case or domain-specific extension of multi-modal sensing, where multiple channels of homogeneous or domain-specific sensors are selectively used for a target task.

Do not treat multi-modal sensing and multi-channel sensing as two separate frameworks.

## Framework Name

Use the acronym **CL-TMC** after first defining it as:

**closed-loop framework for task-aware multi-modal sensing control (CL-TMC)**

## Important Positioning

CL-TMC should be positioned as a framework that extends existing sensor/network-level efficiency approaches toward task-performance-feedback-based sensing control.

Existing studies may focus on:

- Multi-modal sensing and sensor fusion
- Energy-efficient sensing
- Sleep scheduling
- Duty cycling
- Adaptive sampling
- Data reduction
- Redundancy-aware sensing
- Network-assisted localization
- Multi-channel biomedical sensing
- Learning-based or optimization-based control

However, CL-TMC is different because it explicitly closes the loop between task performance and sensing control.

## Reinforcement Learning Positioning

Do not present reinforcement learning as the core contribution of the article.

Reinforcement learning can be described as one possible implementation method for CL-TMC, especially when sensing control is modeled as a sequential decision-making problem under uncertainty.

The main contribution of the article is the closed-loop task-aware sensing control framework, not a specific RL algorithm.

If performance results are based on an RL-based controller, describe it as a learning-based implementation of CL-TMC. Do not overemphasize DQN, RL architecture, hyperparameters, or training details in the magazine-style article.

## Use Cases

The article should include two representative use cases:

1. Energy-efficient localization
2. Multi-channel biomedical prediction

The localization use case should illustrate heterogeneous multi-modal sensing control.

The biomedical prediction use case should illustrate domain-specific multi-channel sensing control.

Both use cases should emphasize that CL-TMC can reduce unnecessary sensing, communication, and processing overhead while maintaining task-level performance.

## Figures

Use the figure plan in `figure_plan.md`.

The article will include four main figures:

1. CL-TMC framework architecture
2. Representative use case architectures:
   - (a) energy-efficient localization
   - (b) multi-channel biomedical prediction
3. Performance evaluation for energy-efficient localization
4. Performance evaluation for multi-channel biomedical prediction

Figures should be described in the main text using message-oriented explanations.

## Citation Rules

Do not invent citations.

Use only references included in `references.bib`.

If a citation is needed but no suitable reference exists, write:

`[REF NEEDED]`

Do not fabricate author names, publication titles, venues, years, or DOI information.

## Writing Order

Draft the article in the following order:

1. Introduction
2. Section II: From Data-Centric Data Collection to Task-Aware Sensing Control
3. Section III: Closed-Loop Framework for Task-Aware Multi-Modal Sensing Control
4. Section IV: Use Cases of CL-TMC
5. Section V: Open Research Issues
6. Conclusion
7. Abstract

The abstract should be written after the main sections are drafted.

## Expected Output

If a LaTeX template is available, write the manuscript in LaTeX.

If no LaTeX template is available, first draft the manuscript in Markdown.

Maintain a clear, concise, and magazine-style narrative.