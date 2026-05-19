# II. From Data-Centric Data Collection to Task-Aware Sensing Control (Skeleton)

## II-A. Static and Periodic Sensing Baseline

Many practical IoT systems start from static sensing policies, such as fixed modality sets, fixed sampling intervals, and periodic reporting schedules. This baseline is attractive because it is simple, predictable, and relatively easy to deploy and maintain across large device populations.

However, static sensing policies are largely context-agnostic. They do not explicitly distinguish task-critical sensing data from task-irrelevant sensing data under changing environments, device states, and service requirements. As a result, systems may either overspend resources on unnecessary sensing or under-collect data when task demands rise.

**Citation needs:** [REF NEEDED: static/periodic IoT sensing baseline studies], [REF NEEDED: operational tradeoffs of fixed sensing configurations].

## II-B. Energy-Efficient Sensing and Sleep Scheduling

A substantial body of prior work has improved sensing efficiency through sleep scheduling, duty cycling, and sensor activation control. These mechanisms are important and practical, and they often optimize metrics such as energy consumption, coverage, connectivity, and network lifetime.

From a CL-TMC perspective, the key limitation is that these mechanisms may not directly know whether deactivating a specific sensor will materially affect task-level inference performance (e.g., localization error, prediction confidence, or service QoE). In other words, efficiency gains at the sensor/network layer do not automatically guarantee that task requirements remain satisfied.

**Citation needs:** [REF NEEDED: sleep scheduling in WSN/IoT], [REF NEEDED: duty cycling and sensor activation control], [REF NEEDED: energy/coverage/connectivity/lifetime optimization in sensing networks].

## II-C. Adaptive Sampling and Data Reduction

Another major line of work reduces sensing and communication burden through adaptive sampling, selective acquisition, feature reporting, and compact data representation. These methods are valuable for reducing uplink load and processing overhead in resource-constrained deployments.

Compressed sensing can be included here as one possible data reduction method, but it is not the central framing of this article. CL-TMC is broader: it chooses sensing and data reduction actions based on whether the resulting reduced data remain sufficient for the target task under current system conditions.

**Citation needs:** [REF NEEDED: adaptive sampling for IoT sensing], [REF NEEDED: data reduction and feature reporting], [REF NEEDED: compressed sensing as one possible technique], [REF NEEDED: task-aware sufficiency of reduced sensing data].

## II-D. Redundancy-Aware Collection and Its Limits

Redundancy-aware sensing and correlation-based suppression aim to remove duplicate or highly similar observations, which can significantly reduce communication traffic and sensing cost. This is an important step beyond naive always-on collection.

Still, statistical redundancy is not the same as task irrelevance. Two streams that look correlated may contribute differently when task uncertainty is high, and a stream that appears unique may still have low task value in a specific context. CL-TMC therefore evaluates sensing usefulness through task-level feedback, not correlation structure alone.

**Citation needs:** [REF NEEDED: redundancy-aware sensing/data collection], [REF NEEDED: correlation-aware sensor selection], [REF NEEDED: task-dependent value of correlated sensing streams].

## II-E. Why Closed-Loop Task-Aware Control is Needed

The common gap across the above approaches is the missing closed loop between task outcomes and sensing actions. CL-TMC addresses this gap by feeding task-level indicators back into sensing control so that modality activation, sampling intensity, and transmission behavior can adapt over time under resource and network constraints.

This motivates a shift in system objective: from minimizing sensing cost alone or maximizing data availability alone toward satisfying task requirements with the minimum necessary sensing, communication, and computation cost. This positioning sets up Section III, where the CL-TMC architecture and control dimensions are introduced.

**Citation needs:** [REF NEEDED: task-oriented/semantic communication motivation], [REF NEEDED: closed-loop control for inference-centric systems], [REF NEEDED: joint sensing-communication-computation tradeoff frameworks].
