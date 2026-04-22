# Homeostatic Consensus

**A dynamic, health-weighted consensus model where validator influence is a decaying, continuously re-earned function of capital and non-correlated performance under stress.**

> “Truth is not agreed upon. It survives.”

---

## Overview

Traditional Proof of Stake (PoS) systems equate capital with influence. Over time, this leads to **systemic calcification**—a state where networks continue to produce blocks but lose independence, entropy, and adaptive capacity.

**Homeostatic Consensus** replaces static ownership with a **volumetric lease on influence**.

In this model:

- Power is not a fixed right
- Power decays over time
- Power must be continuously re-earned through **non-correlated performance under stress**

---

## Core Thesis

> A network is not secure because it is large, but because it is alive.

Validator influence should reflect:

- **resilience**
- **independence**
- **ongoing contribution**

—not passive capital accumulation.

---

## Part I: Mechanism (Technical Specification)

### 1. Influence Equation

Effective Power ($EP$) is defined as:
EP_t = log(Stake) × BC_t × e^(-λΔt)


#### Components

- **log(Stake)**  
  Introduces diminishing returns on capital. Prevents linear dominance by large holders.

- **BC (Build Capacity)**  
  A real-time coefficient measuring contribution to system health.

- **e^(-λΔt)**  
  Temporal decay. Authority evaporates without continuous participation.

- **Δt**  
  Rolling time window since last validated contribution.

- **λ (Lambda)**  
  Metabolic rate of the system. Governs memory vs responsiveness.

---

### 2. Build Capacity (BC)

BC is computed using the harmonic mean:

BC = 3 / (1/L + 1/O + 1/D)


All components are normalized to the **[0, 1] range per epoch**.

#### Metrics

| Metric       | Signal       | Description |
|-------------|-------------|-------------|
| **Liveness (L)** | Continuity | Percentage of successful block signatures within the current epoch |
| **Equilibrium (O)** | Resilience | Relative performance during network-wide liveness degradation (e.g. >15% failure) |
| **Diversity (D)** | Entropy | Probabilistic non-correlation based on observable behavior (timing, peer paths, jitter) |

---

### 3. Diversity Model (D)

Diversity is **not identity-based**.

Instead, it is a **probabilistic estimation of independence** derived from observable signals:

- signing jitter patterns  
- peer discovery topology  
- behavioral correlation  

> The system penalizes statistically significant coordination without attempting to infer operator identity.

---

### 4. D-Sigmoid Penalty

To mitigate spoofed diversity (“Surface Entropy Trap”), correlated nodes are penalized using a sigmoid decay function.

- As behavioral similarity increases → D decreases smoothly
- No hard cutoffs or kill-switches
- Encourages **real infrastructure decentralization**

---

### 5. Temporal Decay (Metabolic Model)

Decay ensures:

- no permanent dominance  
- continuous participation requirement  
- dynamic rebalancing of influence  

The system behaves as a **metabolic process**, not a static registry.

---

## Part II: Interpretation (System Philosophy)

### Consensus as an Immune System

Consensus acts as a **regulatory organ**, not just a voting mechanism.

It:

- detects coordination patterns (non-self)
- suppresses centralization pressure
- maintains systemic diversity

Centralization is treated as a **tumor**, not a threshold.

---

### The Digital Hamam (Operator Experience)

While the mechanism is mathematical, the operator experience is designed as a **Digital Hamam**:

- **Purification**  
  Filtering noise and correlated behavior

- **The Tellak (Validator)**  
  Maintains node cleanliness (sovereignty and uniqueness)

- **Homeostasis**  
  A state of low-friction, non-extractive participation

---

## Design Principles

- **No static authority**
- **Decay over accumulation**
- **Correlation over identity**
- **Resilience over throughput**
- **Entropy as a first-class signal**

---

## Known Limitations

- Diversity (D) is an estimation and cannot perfectly infer true independence
- Highly sophisticated actors may approximate non-correlation
- Parameter tuning (λ, thresholds) significantly affects system stability
- Stress-based signals may introduce strategic behavior under certain conditions

---

## Future Work

- Simulation modeling (multi-node adversarial scenarios)
- Attack scenario analysis (Sybil, coordinated clusters, fake diversity)
- Parameter calibration (λ sensitivity, sigmoid curves)
- Real-world testnet implementation

---

## Status

**Release Candidate (v0.9)**  
This is a conceptual and technical specification. Not production-ready.

---

## License

MIT (or choose appropriate license)

---

## Author

Mehmet Orkun Alabaz  
https://orqon.com

---

## Closing

> Power is not something you own.  
> It is something you sustain.

**Prove. Sustain. Earn. Repeat.**