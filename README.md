# Responsibility Closure Loop (RCL)

This repository provides a **machine-readable framework** to ensure that
**judgment and responsibility are not skipped** in system design.

It does not automate decisions.  
It enforces that decisions are explicitly owned and closed by humans.

---

## What this is

This repository contains:

- A **minimal Responsibility Manifest template** (YAML)
- A **fixed AI Auditor prompt** that reviews responsibility gaps
- A **design flow** that forces responsibility closure (Human → AI → Human)

It is a **toolkit** to operationalize VCDesign principles in real design work.

---

## What this is NOT

- ❌ A system generator
- ❌ An optimization framework
- ❌ An AI decision engine
- ❌ A best-practice catalog

This repository will not tell you *what to decide*.  
It only prevents you from **skipping the act of deciding**.

---

## Constitution

VCDesign is a philosophy that, in an always-on high-speed optimization environment,
designs where judgment and responsibility reside to sustain the value humans and systems create.
Its implementation attitude is regeneration-premise design.

---

## Background Philosophy

We assume the environment is:

> **Always-On High-Speed Optimization**

In such an environment:
- Systems are constantly regenerated
- Implementations change faster than design intent
- AI can easily bypass human judgment

VCDesign addresses this by designing **where judgment and responsibility live**.

This repository implements that philosophy as an operational form.

---

## Core Concept: Responsibility Closure Loop

All design decisions are expressed and reviewed through the following loop:
P → D → Δ → R

- **P (Preconditions / Promise)**  
  What must be true, and what must never be decided automatically

- **D (Do / Decision / Display)**  
  Execution, UI, batch, or AI assistance (never final judgment)

- **Δ (Delta)**  
  Facts indicating that P is not fulfilled  
  (not executed, delayed, unverified, boundary violation, no evidence)

- **R (Resolution)**  
  Explicit closure of responsibility  
  (stop, return to human, trigger review, close by root cause)

> A design is incomplete as long as any unresolved Δ exists.

---

## Fixed Principles (Constitution)

The following principles are **non-negotiable**:

- A Delta (Δ) always requires Resolution (R)
- Boundary violations must stop execution
- No evidence means no final decision
- Resolution cannot be skipped
- Root-cause closure may resolve multiple symptom deltas

These principles are **not configuration options**.

---

## Design Flow (Human → AI → Human)

### Step 1: Human defines responsibility

The designer writes a **Responsibility Manifest** describing:
- What value must be preserved
- Where judgment is allowed or forbidden
- What must be true before proceeding

This step cannot be delegated to AI.

---

### Step 2: AI audits, does not decide

An AI Auditor reviews the manifest and:
- Detects ambiguous Preconditions (P)
- Detects missing or weak Delta (Δ)
- Detects paths where Resolution (R) could be skipped
- Detects violations of fixed principles

The AI:
- ❌ does not decide
- ❌ does not propose solutions
- ❌ does not optimize

It only returns **questions**.

---

### Step 3: Human closes responsibility

The designer:
- Answers the questions
- Accepts or rejects risk
- Explicitly chooses Resolution (R)

Only then can the design proceed.

---

## Repository Structure
.
├─ manifests/
│ └─ responsibility_manifest.template.yaml
├─ prompts/
│ └─ auditor.prompt.md
├─ examples/
│ └─ sample_manifest.yaml
└─ README.md


- `manifests/` : Human-authored responsibility definitions
- `prompts/`   : Fixed AI auditor behavior (design rule)
- `examples/`  : Reference usage

---

## Relationship to VCDesign

- **VCDesign** defines the philosophy and fixed principles (WHY / WHAT)
- **Responsibility Closure Loop** provides an operational form (HOW)

This repository depends on VCDesign principles,  
but VCDesign does not depend on this repository.

---

## One-line summary

> **This system does not design for you.  
> It prevents you from skipping design responsibility.**

---

## Context

This repository is part of a broader design philosophy exploring
how responsibility, boundaries, and decision-making should be handled
in AI-assisted systems.

- VCDesign (design philosophy & architecture):
  https://vcdesign.org/

This project can be used independently.
Understanding VCDesign is not required.
