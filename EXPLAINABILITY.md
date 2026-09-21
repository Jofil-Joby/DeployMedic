## Decision and Reasoning

DeployMedic decides whether the project exposes a recognizable deployment configuration artifact. Missing evidence becomes a deployment-readiness finding with a conditional recommendation.

## Inputs and Data Sources

It checks the project file list for Dockerfile, vercel.json, render.yaml, or fly.toml. The decision is intentionally based on visible deployment metadata.

## Limits and Constraints

It cannot know whether a project actually requires deployment configuration or whether deployment is managed entirely outside the repository. Cloud-console settings and CI secrets are outside its evidence.
