# AI for Security

## Multi-Model Vulnerability Discovery

The Georgian research session explored how much vulnerability-discovery performance depends on the model itself versus the surrounding harness, prompting, and context.

The workflow presented followed a staged pattern:

**Scan → Process → Revalidate → Review / Map → Confirm**

Initial model output was not treated as ground truth. Findings were investigated, revalidated, deduplicated, mapped to root causes, and then confirmed.

## Speaker-Presented Study Figures

The presentation referenced:
- **24 model / runner configurations**
- **2 runs per configuration**
- **265 confirmed security root causes**

These are speaker-presented figures, not independently reproduced results in this repository.

## Practical Findings

### One run is not enough
Repeat runs can surface additional findings, and no single run should be treated as complete coverage.

### Different models find different bug classes
The talk showed meaningful variation across vulnerability classes such as policy bypass, SSRF / host injection, denial-of-service / resource issues, secrets / credentials, and authentication / authorization.

### Cost per confirmed finding matters
Useful evaluation should combine coverage, false-report rate, confirmed findings, and economics rather than focusing only on raw capability.

### Prompt engineering matters
A more engineered security prompt improved results across several model families in the speaker's tests.

### Better context can lift weaker models
Targeted context included call graphs, entry points, callers / callees, attacker-controlled inputs, sinks, data flow, guards, control flow, and code-property-graph style information.

The important lesson was: **more context is not automatically better context.**

## Practitioner Interpretation

A practical security workflow would:
1. Use more than one model where economics allow.
2. Run important analyses more than once.
3. Revalidate findings.
4. Track false positives explicitly.
5. Optimize for cost per confirmed finding.
6. Use targeted context rather than indiscriminate context expansion.
7. Build a model portfolio around vulnerability coverage rather than one leaderboard score.
