# Architecture overview

PeakGuard AI separates demand forecasting from peak-risk detection. The forecast answers a numerical planning question; the risk assessment supports prioritization. Keeping these responsibilities distinct makes it possible to discuss forecasting error and missed-risk events separately.

## Information flow

The high-level flow is input validation, prediction, risk-state presentation, and human review. This description deliberately omits the underlying data schema, feature definitions, model families, fitted parameters, and decision thresholds.

Input validation needs to consider when observations become available, as well as when they were measured. A correctly ordered timestamp alone does not prove that a measurement was available at prediction time. Missing, delayed, or inconsistent inputs require an explicit operational policy before deployment.

The forecasting component estimates upcoming demand. The risk component assesses whether a period deserves additional attention. This portfolio does not claim that the forecast is an input to the classifier or disclose how either component is implemented.

## Human-facing risk states

ALERT indicates higher-priority review. WATCH supplies an additional safety buffer for attention. An unflagged period can still contain a missed event. WATCH has no claimed conformal coverage, calibrated probability guarantee, or safety certification.

An operator would need context beyond a prediction before changing production activity. Equipment constraints, production requirements, and authorization to act are outside the scope of this documentation. No automatic control integration is claimed.

## Deployment questions left open

Operational use would require checking data arrival times, handling unavailable inputs, monitoring changes in operating conditions, and assigning responsibility for responding to warnings. These are requirements for future validation, not claims that a deployed system already satisfies them.
