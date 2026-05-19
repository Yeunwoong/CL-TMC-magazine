# V. Open Research Issues for CL-TMC (Skeleton)

## V-A. Task-Performance Modeling and Metric Design

A core challenge is not only defining task indicators that are decision-useful and operationally measurable (e.g., uncertainty, confidence, error, QoE), but also modeling how sensing actions influence those indicators over time.

In particular, CL-TMC needs practical models that connect modality/channel selection, sampling rate, and data representation choices to downstream task-level behavior under changing context and resource constraints.

**Citation needs:** [REF NEEDED: task-level metric design in inference systems], [REF NEEDED: models linking sensing actions to task performance].

## V-B. Controller Methodology Selection

CL-TMC can be implemented by multiple methodology families, and the key issue is selecting an approach that matches system constraints and deployment goals.

Rule-based control is often interpretable and lightweight, making it attractive for constrained devices, but it may have limited adaptability in dynamic environments. Optimization-based control can provide structured and often interpretable decisions when models are reliable, but complexity and model mismatch can limit robustness. Online learning or contextual bandits can support incremental adaptation with moderate complexity and reduced long-horizon burden, though they still require careful exploration and feedback design. Reinforcement learning can handle sequential adaptation under uncertainty and delayed effects, but it may require more data, tuning effort, and deployment safeguards.

The open problem is methodology selection across interpretability, computational complexity, online/offline operation mode, data requirements, and adaptability—while keeping CL-TMC framework goals central rather than centering any single algorithm family.

**Citation needs:** [REF NEEDED: rule/optimization-based adaptive sensing], [REF NEEDED: bandit/online learning for sensing control], [REF NEEDED: RL in resource-aware sensing], [REF NEEDED: comparative studies on control-method tradeoffs].

## V-C. Feedback Delay, Stability, and Network Coupling

In practical systems, task feedback can be delayed, noisy, partial, or inconsistent across sensing and network timescales. Under such conditions, closed-loop sensing updates can become unstable or systematically suboptimal if the controller reacts to stale or unreliable indicators.

Designing robust CL-TMC operation therefore requires delay-aware and uncertainty-aware feedback handling, together with network-coupled control logic that remains stable under fluctuating communication conditions.

**Citation needs:** [REF NEEDED: delayed feedback control], [REF NEEDED: network-aware closed-loop sensing], [REF NEEDED: stability under noisy/partial feedback].

## V-D. Data, Benchmarking, and Evaluation Protocols

CL-TMC needs evaluation datasets and protocols that go beyond static prediction benchmarks. In addition to sensing signals and task labels, useful CL-TMC datasets should include sensing costs, selected sensing actions, device/network states, and task feedback traces over time.

Without these elements, it is difficult to evaluate closed-loop behavior, adaptation quality, and real system tradeoffs between task performance and sensing/communication/computation overhead.

**Citation needs:** [REF NEEDED: benchmarking adaptive sensing systems], [REF NEEDED: datasets with sensing-cost annotations], [REF NEEDED: time-series feedback/action traces for closed-loop evaluation].

## V-E. Scalable Deployment and Edge-Cloud Partitioning

A key deployment question is how to partition CL-TMC functions across device, edge, and cloud layers. Lightweight and latency-sensitive decisions may run on-device, while more complex inference pipelines or policy updates may be executed at the edge/cloud.

The open issue is finding partition strategies that satisfy latency, reliability, energy, and scalability targets while preserving consistent task-feedback-to-sensing control behavior across tiers.

**Citation needs:** [REF NEEDED: edge-cloud partitioning for sensing/inference pipelines], [REF NEEDED: hierarchical control deployment in IoT systems].

## V-F. Standardization and Interoperability

For broad adoption, CL-TMC requires standardized interfaces across heterogeneous platforms. This includes interfaces for sensing capabilities, sensing cost descriptors, task-level feedback signals, network telemetry, and sensing control commands.

Interoperability at these interfaces can reduce integration overhead, improve portability of control logic, and support multi-vendor deployment of task-aware sensing systems.

**Citation needs:** [REF NEEDED: interoperability standards for IoT sensing/control], [REF NEEDED: interface models for cross-layer sensing feedback systems].
