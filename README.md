# DeployMedic

> Portable agent for detecting missing recognizable deployment configuration.

## What it does

DeployMedic inspects a project for common deployment descriptors such as Dockerfile, Vercel, Render, or Fly configuration. When none is visible, it produces an evidence-backed recommendation rather than assuming how the project is deployed.

### Diagnostic fingerprint

**Deployment artifact discovery → release-readiness signal → evidence → action**

## Why this agent is distinct

DeployMedic focuses on the deployment boundary. It does not attempt to infer a cloud architecture from a README or guess which hosting platform the project uses.

## Workflow

```text
Project
   ↓
Deployment-config detector
   ↓
Release-readiness rule
   ↓
Evidence
   ↓
Deployment improvement plan
```

## Verification

Includes OpenGAP-compatible metadata, a deployment-focused fixture, four portability adapters, explainability contracts, and automated adapter tests.

OpenGAP validation passed and all four generated framework exports have been exercised successfully.

## Design principle

**Detect before assuming.** The agent identifies visible deployment configuration and clearly communicates when the repository does not expose enough evidence.

## Medic family

DeployMedic is one specialized release-engineering component in the larger Medic family.