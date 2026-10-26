# Hybrid PQC–MDN Research

**Role:** Student research participant — experiment setup, troubleshooting and result interpretation with guidance  
**Context:** Faculty-led research with Dr. Ma  
**Stage:** Preliminary research experiment  
**Software used in the project:** Existing Python research scripts involving PyTorch, Qiskit and NumPy

## Research question

Can features from a parameterized quantum circuit (PQC) improve probabilistic modeling of received power versus distance compared with a classical mixture density network (MDN)?

## My involvement

- Set up the project's Python environment, installed required dependencies and executed existing research code with step-by-step assistance.
- Worked through errors and numerical issues while running the comparison, including `NaN` overlap-area values.
- Made guided changes to numerical evaluation settings to obtain usable overlap-area results.
- Examined training and validation negative log-likelihood, fitted density curves and statistical comparisons.
- Checked consistency between PyTorch-generated and Qiskit-generated PQC features at sampled distances.
- Saved experimental results for further discussion with the research team.

**Programming context:** I have hands-on exposure to executing, modifying and troubleshooting research scripts, but I am not representing myself as an independent Python, PyTorch or Qiskit developer, and I did not originate the full research model.

## Preliminary results

| Metric | Classical MDN | Hybrid PQC–MDN |
|---|---:|---:|
| Validation NLL | −0.3873853 | **−0.5258318** |
| Average analytic overlap area, 30 distances | 0.7304595 | **0.7805031** |
| Analytic overlap area, 150 m | 0.8671217 | **0.9477702** |
| Generated-sample KDE overlap area, 150 m | 0.8372806 | **0.9646305** |

Maximum sampled PyTorch–Qiskit feature difference: **2.98 × 10⁻⁷**.

**Interpretation:** Lower NLL is better for this comparison; continuous-density NLL can be negative. The hybrid did *not* outperform the classical baseline on every metric. At 150 m, for example, the classical model estimated the mean more accurately while the hybrid estimated variance more accurately.

These are preliminary outputs from a specific run and require more replication and independent validation. Model/code ownership and permission to share datasets should be confirmed with the supervising research team.
