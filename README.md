# NEXUS System Architecture

NEXUS is a unified architectural concept for next-generation computing systems. It combines a compiler-managed execution model, AI runtime optimization, specialized hardware acceleration, and a decoupled memory hierarchy into a single execution fabric.

This repository synthesizes several interrelated ideas into one coherent architecture:

- NEXUS-New-PC-Architecture: overall system and execution design
- OMNI-CORE-v2-NEXUS-FLOW: compiler, task graph, flow semantics, and execution model
- Fourier-Analog-Processing-Unit-FAPU-: analog Fourier-domain acceleration
- MOSRAM: memory redesign and highly specialized storage layer

## Core Thesis

The dominant limitation of current computing systems is not merely raw compute power; it is the architectural bottleneck created by CPU-centric orchestration, fragmented memory access, and the lack of adaptive system-level optimization.

NEXUS argues for a different model:

- user intent is compiled into a structured task graph
- work is dispatched to the most appropriate execution unit
- memory is treated as a managed resource, not just passive storage
- AI acts as a system optimizer and runtime scheduler
- analog and programmable accelerators complement digital compute

## Architecture Layers

### 1. Compiler / Intent Layer
The compiler translates user intent into a dependency-aware task graph. This graph contains execution nodes, data ownership boundaries, resource constraints, and failure paths.

### 2. Scheduler / Runtime Layer
The runtime scheduler decides where each task should run:

- CPU for orchestration and scalar control
- GPU for vectorized parallel operations
- NPU for learned optimization and inference acceleration
- FAPU for analog Fourier-domain compute
- specialized memory paths for data-heavy flows

### 3. Memory Fabric Layer
Memory is separated into multiple categories:

- application memory
- data memory
- page-addressable or virtualized memory
- high-speed buffers for specialized compute units

This reduces the dominance of central CPU memory traffic.

### 4. Specialized Compute Layer
NEXUS includes multiple execution domains instead of one universal compute pipeline. Specialized compute becomes a core architectural concept.

### 5. AI Controller Layer
The AI controller observes runtime behavior such as memory pressure, thermal state, latency, queue length, and success/failure trends. It then optimizes scheduling, workload placement, and system-level policy over time.

## Why This Architecture Matters

This model aims to solve several recurring problems in modern computing:

- CPU bottlenecks
- inefficient memory access
- rigid execution pipelines
- poor workload matching between compute units
- lack of adaptive system optimization

## Repository Contents

- `docs/architecture-overview.md`: high-level system model
- `docs/compiler-flow.md`: compiler and execution semantics
- `docs/memory-hierarchy.md`: memory and storage model
- `docs/analog-compute.md`: analog and Fourier-based compute unit
- `docs/ai-runtime-controller.md`: AI optimization and runtime control
- `docs/parallel-execution-model.md`: concurrency and scheduling model
- `docs/roadmap.md`: future development path
- `paper/NEXUS-System-Architecture.md`: long-form synthesis paper

## Suggested Reading Order

1. `docs/architecture-overview.md`
2. `docs/compiler-flow.md`
3. `docs/memory-hierarchy.md`
4. `docs/analog-compute.md`
5. `docs/ai-runtime-controller.md`
6. `docs/parallel-execution-model.md`
7. `paper/NEXUS-System-Architecture.md`

## Summary

NEXUS proposes a system in which the computer is reimagined as an execution fabric: a coordinated environment composed of compiler planning, specialized compute, managed memory, and AI-based runtime optimization.
