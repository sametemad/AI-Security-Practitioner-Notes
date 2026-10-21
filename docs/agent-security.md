# Production Agent Security

## Security Still Starts with Traditional Controls

The ClickUp session reinforced a useful principle: **AI systems are still computer systems.** Identity, authorization, least privilege, observability, and trust boundaries remain foundational.

## Prompt Injection Is an Integrity Problem

The session treated prompt injection as an unsolved problem. A safer design assumption is to assume compromise may eventually happen and constrain what a compromised agent can do.

## Dual Identity

One of the strongest patterns discussed was separating:
- **Agent identity**
- **Human / user identity**

For sensitive actions, authorization should consider both identities rather than letting the agent inherit the user's full authority.

## Deterministic Authorization

LLMs should not make final access-control decisions. Authorization should remain in deterministic systems such as RBAC, ACLs, ABAC, policy engines, and service-side enforcement.

## Rule of Two / Lethal-Trifecta Thinking

Three dangerous capabilities were highlighted:
1. Reading untrusted content
2. Accessing sensitive data
3. Taking real-world actions

Combining all three sharply increases risk and should trigger stronger external controls.

## Human Approval

Human approval is most useful for irreversible, destructive, high-impact, or permission-changing actions. Approval on every action creates fatigue and weakens the control.

## Graceful Failure

Agents need explicit failure modes such as:
- cannot verify
- reason
- escalate to human

This is safer than indefinite retries or overconfident execution.

## Kill Switch and Observability

A production agent should be disableable quickly. Agent traces and logs are also security-relevant because they may contain prompts, tool arguments, user data, sensitive outputs, and policy decisions.

## Practical Builder Rules

1. Security is a design constraint, not a final gate.
2. Every context boundary is a trust boundary.
3. Ship the kill switch early.
4. Bring security into the design process before autonomy expands.
