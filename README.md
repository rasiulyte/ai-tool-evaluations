# AI Tool Evaluations

Structured assessments of AI development tools from a quality engineering perspective, grounded in current AI safety research and evaluation research.

## Evaluation Framework

This framework combines traditional software QA methodology with AI-specific evaluation approaches from NIST, ISO, and peer-reviewed research (2022-2025).

### Core Evaluation Dimensions

| Category | What I'm Testing | Key Questions |
|----------|------------------|---------------|
| **Verification** | Does it do what it claims? | Does it meet stated capabilities? Are outputs technically correct? |
| **Validation** | Does it solve the real problem? | Is it actually useful in context? Does it improve real workflows? |
| **Accuracy & Reliability** | Correctness + consistency | Are outputs correct? Consistent across similar tasks? |
| **Edge Cases & Robustness** | Where does it break? | What inputs cause failure? How does it handle ambiguity? |
| **Confidence Calibration** | When is it confidently wrong? | Does it know what it doesn't know? Does it hedge appropriately? |
| **Human Vulnerability** | Over-reliance risks | Does it encourage blind trust? Could users be misled? Does it erode skills over time? |
| **Security** | Unsafe outputs | Does it suggest vulnerable patterns? Expose sensitive data? |
| **Explainability** | Can you understand why? | Are suggestions transparent? Can you trace the reasoning? |

### Research Foundation

This framework draws from:
- **NIST AI RMF** — GOVERN, MAP, MEASURE, MANAGE functions for AI risk management
- **NIST ARIA Program** — Sociotechnical testing measuring human-AI interaction impacts
- **Metamorphic Testing** — Testing input/output relationships when ground truth is unavailable
- **Trust Calibration Research** — Studies showing adaptive interventions reduce inappropriate reliance by 38%
- **Automation Bias Literature** — Understanding when users over-defer to AI despite contradictory evidence
- **ISO/IEC 42001:2023** — AI management system standards for governance and risk assessment

## Evaluations

| Tool | Status | Issues | Focus Area |
|------|--------|--------|------------|
| GitHub Copilot | 🔄 In Progress | [View Issues](../../issues?q=label%3A%22github-copilot%22) | Code generation, security patterns |
| M365 Copilot (Word) | 🔄 In Progress | [View Issues](../../issues?q=label%3A%22m365-copilot%22+label%3A%22word%22) | Document creation, template handling |
| M365 Copilot (Excel) | 📋 Planned | — | Formula generation, data analysis |
| M365 Copilot (PowerPoint) | 📋 Planned | — | Presentation creation, content accuracy |

## Quick Stats

- **Total Issues Found:** 3
- **High Severity:** 1
- **Human Vulnerability Concerns:** 2

## Repository Structure
```
/github-copilot
  ├── evaluation-notes.md
  ├── edge-cases.md
  └── findings.md
/m365-copilot
  ├── word/
  │   ├── evaluation-notes.md
  │   ├── edge-cases.md
  │   └── findings.md
  ├── excel/
  │   └── (planned)
  └── powerpoint/
      └── (planned)
/frameworks
  └── evaluation-template.md
```

## Session Log

| Date | Tool | Focus | Key Findings |
|------|------|-------|--------------|
| 2024-12-27 | GitHub Copilot | Security patterns | Password storage gaps, SQL injection prevention works |
| 2025-01-03 | M365 Copilot Word | PDF import + template | (pending your test results) |
