# Project Constitution: Tasks Management System

## Overview
This document serves as the primary governing constitution for the Tasks Management System. It defines our culture, programming principles, and the standard operating procedures for development. We prioritize architectural integrity, reliability, and cloud-native scalability.

---

## Core Programming Principles

### 1. Test-Driven Development (TDD)
- **Red-Green-Refactor:** No production code shall be written without a corresponding failing test.
- **Verification First:** Tests are the primary specification of behavior.
- **Coverage:** We aim for meaningful coverage that validates business logic, edge cases, and agent decision-making paths.

### 2. Documentation-Led Development
- **Official Sources:** Always consult the official documentation for any SDK, framework, or library (e.g., OpenAI Agents SDK, Python MCP, FastAPI, Next.js).
- **Agent Skills & MCP:** Utilize specialized agent skills or Model Context Protocol (MCP) servers to retrieve, index, and apply the most up-to-date documentation and best practices.
- **No Guessing:** If the implementation of a tool or library is unclear, research first.

### 3. Kubernetes (K8s) Perspective
- **Cloud-Native by Design:** Every component must be designed for deployment on Kubernetes from Day 1.
- **Observability:** Implement structured logging, health checks (liveness/readiness probes), and metrics.
- **State Management:** Design for ephemeral environments; state must be managed via external persistence (e.g., Google Sheets, Databases) or distributed state stores.
- **Configuration:** Use environment variables and secret management for all configurations.

---

## The SDD-RI Development Loop
We follow the **Specification-Driven Development with Requirements Integration** loop. Each component must pass through these phases sequentially.

### Phase 1: Explore
**Goal:** Establish shared understanding.
- Define "Why" and "Who."
- Identify dependencies and K8s infrastructure requirements.
- Use `ask_user` for critical design decisions.

### Phase 2: Spec
**Goal:** Define the interface and behavior.
- Document architectural patterns.
- Define clear boundaries between agents.
- *Note: Technical JSON schemas belong in implementation docs, not this Constitution.*

### Phase 3: Plan
**Goal:** Design the verification strategy.
- Draft test cases and acceptance criteria.
- Plan the TDD approach for the component.
- Identify required MCP tools for implementation.

### Phase 4: Implement
**Goal:** Build with precision.
- Strictly follow the TDD cycle.
- Adhere to the SDK/Framework's idiomatic patterns.
- Ensure the component is container-ready.

### Phase 5: Verify
**Goal:** Validate against the Constitution and Spec.
- Run the full test suite.
- Verify K8s compatibility (e.g., resource limits, environment handling).
- Final sign-off against acceptance criteria.

---

## Agent Architecture Standards

### Modular Orchestration
- The system is composed of specialized agents with distinct domains.
- Communication between agents must be robust, authenticated, and resilient to transient failures.

### Resilience and Safety
- **Fail-Fast:** Agents should detect and report failures early.
- **Security First:** Never log sensitive data. Implement "Better Auth" consistently across the ecosystem.

---

## Deployment and Infrastructure
- **Target:** Kubernetes (Production-grade servers).
- **CI/CD:** Automated verification and containerization are mandatory.
- **Scalability:** Components must be horizontally scalable whenever possible.

---

**Version:** 2.0 (Refactored to Constitution)  
**Status:** Active & Binding