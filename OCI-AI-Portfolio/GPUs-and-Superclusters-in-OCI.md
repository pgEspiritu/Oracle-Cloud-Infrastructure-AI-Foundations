# RDMA and OCI Supercluster Architecture

Welcome to the **First Principles** video and blog series, where we explore the architectural foundations behind **Oracle Cloud Infrastructure (OCI)** services.  
At OCI, we take pride in delivering **maximum performance** at the **lowest possible cost** to customers.

---

## What is RDMA?

**Remote Direct Memory Access (RDMA)** is a core technology behind many OCI services since the beginning.  
It enables **data transfer or network communication** that **bypasses the CPU**, allowing data to move directly from one machine to another **without CPU intervention**.  

This design delivers:
- **Extremely low latency**
- **High bandwidth**
- **Low CPU overhead**

RDMA forms the **foundation** of:
- **Database services** such as **Exadata Cloud Service (ExaCS)** and **Autonomous Database**
- **HPC workloads**
- **GPU workloads**

---

## Why RDMA Matters in OCI

A few years ago, OCI made a **strategic bet on RoCE** — **RDMA over Converged Ethernet**.  
OCI’s Ethernet fabric now enables RoCE, allowing **HPC**, **GPU**, and **database workloads** to run seamlessly over RDMA networks.  

In partnership with **NVIDIA**, OCI continues to push the limits of **large-scale GPU workloads** — spanning **thousands or even tens of thousands of GPUs** — interconnected in a single **RDMA network** known as a **Supercluster**.

---

## RDMA Supercluster Overview

The **RDMA Supercluster** is an architectural design enhancement that supports **very large GPU workloads** within a **single lossless RDMA fabric**.

### GPU Node Configuration

Each GPU node consists of:
- **8 NVIDIA A100 GPUs**  
- Interconnected via **NVIDIA NVLink**

Each node connects to the **network fabric** at:
- **1.6 terabits per second (1,600 Gbps)** total bandwidth  
- That’s **200 Gbps per GPU**

### Non-Blocking Fabric

The **network fabric** provides a **non-blocking interconnect**, meaning:
- Any GPU can communicate with any other GPU simultaneously  
- All nodes get the bandwidth they need without contention  

---

## Fabric Design: The Three-Tier Clos Network

The **Supercluster** is built using a **three-tier Clos network design**, scaled across multiple **blocks**:

- **Block 1 → Block N**  
- Each block has **two tiers of Clos fabric**  
- Designed to **scale to tens of thousands of GPUs**, with potential for **100,000+ GPUs**

This design ensures massive scalability while maintaining performance consistency.

---

## Managing Latency in Large Networks

### Latency Insights
- **Within a single block:** ~**6.5 microseconds round trip**
- **Across the entire Supercluster:** ~**20 microseconds round trip**

Despite increased latency at scale, these numbers remain **10–20× faster** than typical **virtualized cloud networks**.

### How OCI Manages Latency

To address higher latency, OCI ensures:
- **Quality of Service (QoS)** is enabled across the network  
- **Switch silicon and chipsets** are tuned with **sufficient buffering**  
- Proper **queue allocations** for GPU workloads  
- A **lossless RDMA network** with **intelligent congestion notifications**

---

## Lossless RDMA Networking

**Lossless networking** means:
- **No packet drops**
- **Switches** manage congestion using **notification systems**
- **Buffers** are tuned for **worst-case latency** conditions

This ensures **reliable**, **high-performance** data transfers, even at extreme scale.

---

## Balancing Scale and Latency with Placement

OCI’s **control plane** uses **intelligent placement algorithms** to balance **latency** and **scale**.

### Example:

- **Small workloads (e.g., HPC or database clusters)**  
  → Deployed within a **single block** for minimal latency (~6.5 µs)

- **Large workloads (e.g., GPU Superclusters)**  
  → Spanning multiple blocks (~20 µs latency), but intelligently optimized using **placement hints**

This balance ensures:
- **Low latency** where needed  
- **Scalability** when required  

---

## Network Locality and Placement Hints

OCI introduces **network locality hints** to help customers optimize workload placement.  
These hints allow **GPU topologies** to take advantage of network proximity for better performance.

### Example Scenario:
- A workload spans **two blocks**, each with **multiple top-of-rack (ToR) switches**.
- Using **locality hints**, the workload ensures:
  - **85% of traffic remains local** within each block
  - Only a small fraction crosses blocks (higher latency paths)
  - Average latency remains **significantly lower**
  - **Half of traffic** may experience < **6.5 µs** latency (local ToR communication)

This **network-aware topology** provides both **low latency** and **high throughput**.

---

## Benefits of Locality Optimization

By constraining traffic within **ToR switches** and **blocks**, OCI reduces:
- **Flow collisions** (where two flows compete for the same link)
- **Network congestion**
- **Overall latency**

This optimization leads to:
- **Higher throughput**
- **Improved stability**
- **Better scaling for distributed AI workloads**

---

## Summary

OCI’s **RDMA Supercluster** is a **three-tier Clos network** designed with:
1. **Tuned buffers** to maintain **lossless communication** even at high latency diameters  
2. **Intelligent placement mechanisms** in the **control plane** for low-latency deployment  
3. **Locality hints** for optimizing multi-block workloads and minimizing cross-block latency  

Together, these features deliver:
- **High scalability**
- **Low latency**
- **Lossless performance**
- **Efficient GPU and HPC workload orchestration**

