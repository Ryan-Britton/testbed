# RKD-02: Claude SDK (Autonomous) + Pydantic-AI (Interactive)

**Status:** Accepted
**Source:** VISION.md D2

## Decision

Use Claude Agent SDK for autonomous pipeline agents and Pydantic-AI for interactive console agents.

## Rationale

SDK provides battle-tested file tools, worktree cwd, CLAUDE.md loading for autonomous work. Pydantic-AI provides AG-UI streaming to CopilotKit for interactive chat.

## Alternatives Considered

SDK-only (no AG-UI streaming), Pydantic-AI-only (must rebuild file tools).
