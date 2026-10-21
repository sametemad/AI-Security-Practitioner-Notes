# Agent Skills & MCP Security

## Skills Are Executable Trust Surfaces

The Agent Skills session challenged the idea that a skill is just a Markdown instruction file. A skill package may include scripts, templates, assets, hooks, MCP integrations, nested skills, dependencies, and external URLs.

The practical point: format standardization does not create trust.

## Instructions Can Be the Payload

A malicious skill does not necessarily need a traditional binary exploit. If the agent treats instructions as executable guidance and has access to Bash, files, credentials, environment variables, external tools, or MCP servers, malicious natural-language instructions can become part of the attack path.

## Install-Time Scanning Is Not Enough

A skill can change after initial review because dependencies, remote resources, URLs, package contents, or runtime behavior can change.

## Practical Control Sequence

1. **Scan** the package and instructions.
2. **Inspect** scripts, dependencies, URLs, and requested capabilities.
3. **Sandbox** unknown or untrusted execution.
4. **Restrict** filesystem, network, secrets, and tool access.
5. **Pin** versions where possible.
6. **Monitor** runtime behavior.
7. **Reassess** trust when dependencies or remote resources change.

## Tools Mentioned

The presentation referenced examples including NVIDIA SkillSpecter, Cisco AI Agent Security Scanner, Anthropic skill-scanning approaches, and Skills Patrol.

## Compare Declared Behavior to Actual Behavior

A useful review model is:
- What does the skill say it does?
- What files does it contain?
- What tools can it call?
- What network destinations can it reach?
- What secrets can it access?
- What does it actually do at runtime?

## Memory Integrity

The Q&A also raised the possibility that malicious skills may influence persistent memory or future agent behavior if skill-derived information is written into memory without strong trust controls.

## Practitioner Interpretation

Agent Skills and MCP integrations should be treated like third-party software: least privilege, provenance checks, version control, sandboxing, runtime policy, egress restrictions, secret isolation, logging, revocation, and update review.
