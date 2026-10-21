# Portfolio Follow-On Ideas

These ideas are inspired by the security patterns discussed during the event. They are future portfolio concepts, not implementations included in this repository.

## Secure Agent Tool & Skill Gateway

A future lab could demonstrate a control plane between an AI agent and its tools.

### Proposed Architecture

Untrusted Input  
→ AI Agent  
→ Agent Identity + User Identity  
→ Policy Enforcement  
→ Skill / Tool Security Check  
→ Sandbox  
→ MCP / Tool Gateway  
→ Human Approval for High-Risk Actions  
→ Execution  
→ Audit Log

## Controls to Demonstrate

- Dual identity authorization
- Deterministic policy enforcement
- Tool allowlisting
- Skill manifest inspection
- Secret-access detection
- Sandbox execution
- Prompt-injection containment
- Human approval for destructive actions
- Kill switch
- Audit logging
- Graceful human handoff

## Relationship to Existing Portfolio Work

This concept would complement a cloud-native agent-governance project by focusing specifically on Agent Skills, tool execution, MCP supply-chain risk, sandboxing, runtime permissions, and prompt-injection containment.
