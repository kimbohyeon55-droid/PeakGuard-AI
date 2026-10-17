# Development workflow

The project direction emphasizes traceable decisions and preservation of research evidence. This overview describes the approach without releasing experiment reports or their results.

## Define the decision before the experiment

Start with the intended prediction use, the available information, and the consequences of missed events and false alarms. Define evaluation and acceptance criteria before inspecting candidate outcomes. A favorable result on one measure is insufficient to establish suitability for the intended use.

## Respect time boundaries

Use chronological evaluation for a forecasting problem. Training outcomes must belong strictly before the validation period begins, and inputs must be available at prediction time. Historical decision-rule selection must not consume labels from the period being evaluated.

These principles also apply to preprocessing and derived inputs. This portfolio describes the required discipline; it does not publish audit counts or certify an implementation.

## Preserve comparisons

Keep a retained baseline separate from experimental candidates. Make changes in isolated versions, record their intended purpose, and preserve the evidence used to assess them. A diagnostic candidate is not automatically a replacement for a retained model.

Once a version is frozen, preserve it. Subsequent documentation work should not change the research artifacts it describes. Reproduction requires the authorized data, implementation, environment, and experiment records; this public edition intentionally does not contain those materials.

## Separate analysis from intervention

Examining where errors occur can improve understanding without proving that an operational intervention will work. Simulated schedule changes do not establish causal effects or realized savings. Such claims would need separate evidence.

## Review publication independently

Technical usefulness does not establish redistribution permission. Review proposed public files, their provenance, and publication rights separately from model quality. Keep private records and repository history outside the release, and obtain human approval for the exact proposed contents.
