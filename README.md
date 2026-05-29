# Enterprise SE Technical Exercise Starter Repo

This repository contains a small Flask + Postgres todo application intended for use for SE technical exercise.

## Scenario

A customer has a small Python application that runs locally with Docker Compose. It works, but the application container and dependency setup are not aligned with their supply chain and container hardening goals.

The exercise for the candidate is to improve this application by:

- migrating the application container to Chainguard Containers
- configuring Python dependency installation to use Chainguard Libraries only
- preserving a simple local developer workflow with Docker Compose
- making practical, high-impact improvements without over-engineering the solution

## Timebox

- Expected: 90 minutes
- Max: 2 hours

## Starter repo notes

This starter intentionally includes several issues for the candidate to evaluate and improve. Examples include container image choice, build structure, dependency installation, runtime posture, and local orchestration behavior.

## Run locally

```bash
docker compose up --build
```

Then open <http://localhost:8000>.

## Candidate deliverables

Candidates should submit:

1. Updated code and configuration
2. A short write-up describing:
   - what they changed
   - why they changed it
   - what risks or issues were reduced
   - tradeoffs they made
   - what they would do next in a real customer engagement

## Interviewer notes

A strong solution will usually:

- use appropriate Chainguard Python image variants
- separate build and runtime concerns sensibly
- remove unnecessary packages and dependencies
- avoid running as root
- keep `docker compose up --build` working
- clearly explain prioritization and tradeoffs

