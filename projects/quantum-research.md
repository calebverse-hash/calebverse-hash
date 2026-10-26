# Hybrid PQC–MDN Research

**Role:** Student researcher / experiment implementation  
**Context:** Faculty-led research with Dr. Ma  
**Stage:** Research prototype and preliminary evaluation  
**Tools:** Python, PyTorch, Qiskit, NumPy

## Research question
Can features from a parameterized quantum circuit (PQC) improve a mixture density network's probabilistic modeling of received power across distance compared with a classical MDN?

## Contributions
- Set up and debugged a Python/Qiskit research environment and model comparison experiments.
- Evaluated training and validation negative log-likelihood, estimated probability densities, and overlap-area metrics.
- Used the target transformation `u = log10(Prx + 2.0)` and accounted for the transformation in original-unit evaluations.
- Fixed `NaN` overlap-area evaluations by adjusting numerical integration grids.
- Compared PQC output features between PyTorch and Qiskit and exported evaluation datasets.

## Preliminary results

| Metric | Classical MDN | Hybrid PQC–MDN |
|---|---:|---:|
| Validation NLL | −0.3873853 | **−0.5258318** |
| Average analytic overlap area, 30 distances | 0.7304595 | **0.7805031** |
| Analytic overlap area, 150 m | 0.8671217 | **0.9477702** |
| Generated-sample KDE overlap area, 150 m | 0.8372806 | **0.9646305** |

Maximum sampled PyTorch–Qiskit feature difference: **2.98 × 10⁻⁷**.

**Interpretation:** Lower NLL is better. Continuous density NLL can be negative. The hybrid did *not* outperform the classical baseline on every metric: at 150 m the classical model estimated the mean more accurately, although the hybrid model estimated variance more accurately.

These are **preliminary results from a specific experiment**, not peer-reviewed evidence of general superiority. Repeated seeds and further baselines are needed. Code/data should be shared only with supervisor approval.
