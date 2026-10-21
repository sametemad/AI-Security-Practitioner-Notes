# Key Takeaways

## 1. AI Security Has Two Directions

Modern AI security requires both **AI for Security** and **Security for AI**.

## 2. Vulnerability Discovery Benefits from Diversity

Use multiple models where justified, rerun important analyses, validate independently, measure false positives, and track cost per confirmed result.

## 3. Context Is a Security-Control Variable

Targeted context such as call graphs, data flow, sinks, and attacker-controlled inputs can be more useful than simply increasing context size.

## 4. Prompt Injection Must Be Contained Architecturally

Secure architecture should limit what the agent can read, which secrets it can access, which tools it can invoke, what actions it can perform, and what changes require human approval.

## 5. Identity Separation Matters

An agent should not simply inherit a user's authority. Agent and human identities should be separate, with sensitive actions satisfying both policy contexts.

## 6. Authorization Must Stay Deterministic

LLMs can interpret context but should not be the final authority for access control.

## 7. Agent Skills Are a Supply-Chain Problem

Skills, MCPs, scripts, and external resources introduce dependency, update, provenance, prompt-injection, credential, and runtime-behavior risk.

## 8. Runtime Controls Matter

Security should include sandboxing, egress control, secret isolation, version pinning, runtime monitoring, audit logging, and revocation.

## 9. Human Approval Should Be Selective

Approval is most useful for high-impact or irreversible actions.

## 10. Fail Safely

Agents need explicit failure states and human escalation.

## Bottom Line

**Identity + deterministic policy + least privilege + runtime isolation + observability + human control for high-risk actions.**
