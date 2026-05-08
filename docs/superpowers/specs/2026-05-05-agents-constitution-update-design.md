# Design Spec: AGENTS.md Constitution Updates

**Date:** 2026-05-05
**Topic:** Integrating "Superpowers" principles and "Always Verify" mandate into the project constitution.

## Goal
To evolve `AGENTS.md` from a standard constitution into an AI-native "Superpowers" document that prioritizes rigorous planning, granular execution, and immediate verification.

## Architecture & Principles

### 1. Core Programming Principles Updates
- **Principle 1: Test-Driven Development (TDD) + Immediate Verification**
  - Merge the TDD cycle with the requirement for immediate evidence.
  - *New Rule:* "A task is not 'done' until its behavioral correctness is confirmed with terminal output or test logs. Evidence before assertions."
- **Principle 4: Think Before You Build (New)**
  - Formalize the Research -> Strategy -> Execution lifecycle.
  - *New Rule:* "Always validate assumptions and research official documentation before proposing or applying changes. Planning prevents expensive chaos."

### 2. SDD-RI Development Loop Enhancements
- **Phase 1: Explore (Socratic Refinement)**
  - Integrate iterative questioning. "Use a Socratic approach to interview the goal; uncover edge cases, empty states, and configuration requirements before planning."
- **Phase 3: Plan (Granular Decomposition)**
  - Define the scale of tasks. "Break implementation into micro-tasks (2–5 minutes each). Every task must include a specific verification step and identified file paths."
- **Phase 5: Verify (Evidence-Based Completion)**
  - Strengthen the exit criteria. "Verification is the only path to finality. Claims of success must be supported by the project's specific build, lint, and test tools."

### 3. Tech Stack Standards (New)
- **Primary Language:** Python 3.12+
- **Package Manager:** `uv`
  - *Rule:* Use `uv` for environment management, dependency resolution, and running scripts (`uv run`). Always prefer `uv` over standard `pip` or `venv` to ensure fast, reproducible builds.

## Implementation Strategy
- Surgical updates to `AGENTS.md` using the `replace` tool.
- Ensure formatting remains consistent with the existing GitHub-flavored Markdown.

## Verification Plan
- **Self-Review:** Ensure no "TBD" or vague language exists in the final `AGENTS.md`.
- **Consistency Check:** Verify that the "Superpowers" rules don't contradict existing K8s or Documentation-led principles.
