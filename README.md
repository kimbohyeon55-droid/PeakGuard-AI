# PeakGuard AI

**Industrial electricity forecasting and peak-risk decision support.**

PeakGuard AI explores how forecasting and risk detection can help people review electricity demand in manufacturing. The project considers two related questions: what demand might come next, and which periods deserve closer attention because of peak risk?

This repository is a **documentation-only portfolio**. It presents newly written, high-level descriptions of the project and its engineering approach. The implementation, data, model settings, evaluation results, and visual artifacts are withheld pending publication-rights clearance. Readers cannot run or independently verify the model from this repository.

## Purpose

Changes in production activity can create uneven electricity demand. Forecasting supports planning, while peak-risk detection helps prioritize review. A useful decision-support workflow must consider both missed events and unnecessary warnings, alongside uncertainty about future operating conditions.

The intended user is a person reviewing operational decisions. This portfolio makes no claim of factory deployment, automatic equipment control, or demonstrated electricity savings.

## Architecture

| Component | Responsibility |
|---|---|
| Input validation | Check time ordering, completeness, and whether information is available when a prediction is issued. |
| Forecasting | Estimate upcoming electricity demand. |
| Peak-risk detection | Produce a separate risk assessment for potentially high-demand periods. |
| Decision support | Present risk states for human review. |
| Evaluation and recordkeeping | Keep development decisions, limitations, and retained versions traceable. |

**ALERT** identifies periods requiring higher-priority review. **WATCH** provides an additional safety buffer for attention. WATCH does not represent a statistical coverage guarantee. These labels support judgment; they do not certify safe operation. Numerical decision rules are outside this publication's scope.

## My contributions

I defined the project objectives and the constraints for chronological evaluation, model selection, and publication. I required explicit checks against future-information leakage, comparison with a retained baseline, and preservation of frozen research versions.

I also set acceptance criteria for experiments and required limitations to accompany reported outcomes. For this portfolio, I chose to withhold material whose publication rights remain uncertain and to require a final human review before release. These are documented project-direction contributions; they do not imply sole authorship of every implementation artifact.

## AI-assisted development workflow

The workflow uses explicit requirements, bounded experiments, reviewable artifacts, and human decisions. AI assistance is treated as support for engineering work, with generated material subject to verification.

Codex assisted with inspecting local project records, drafting this English documentation, and preparing the publication audit. Those activities are directly supported by the project conversation. This portfolio does not attribute specific original model code or training runs to Codex where that attribution has not been established. It claims no measured productivity gain or OpenAI endorsement.

## Read the portfolio

- [Architecture](docs/ARCHITECTURE.md): component responsibilities and operational assumptions.
- [Development workflow](docs/DEVELOPMENT_WORKFLOW.md): evaluation discipline and version preservation.
- [AI assistance](docs/AI_ASSISTANCE.md): supported attribution and human responsibility.
- [Publication scope](docs/PUBLICATION_SCOPE.md): exclusions, availability, and rights limitations.

No installation, account, API key, or paid service is needed to read these Markdown documents. There is no executable pipeline or dependency installation in this edition.

## Limitations

Historical observations cannot establish performance at other facilities or under future operating conditions. Input availability and collection latency require operational verification. Prediction errors and false alarms remain possible, and statistical association does not establish a causal effect.

Any discussion of schedule changes is conceptual decision support or model-based simulation, not evidence of realized savings. This edition publishes no performance claims, experimental outcomes, screenshots, or benchmark evidence. No open-source or open-content license is granted in this package.
