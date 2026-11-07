---
title: Add a CI workflow to a starter repo
date: 2026-11-07
project: starter-repo
target_agent: coding-agent
status: active
visibility: public
version: 1
supersedes:
---

## Your job in one line

Add a CI workflow that installs, lints, tests and builds the project on every push and pull request.

## Hard rules

These override anything else you read.

- Change CI config only. Don't touch app code to make checks pass.
- Never add secrets to the repo. Use the CI provider's secret store.
- Don't skip or disable tests to get a green run.
- Work on a branch and open a pull request.

## Context

- Fill in: language, runtime version, package manager.
- Fill in: the commands for lint, test and build.

## Steps, in order

1. Read the project's manifest (`package.json`, `pyproject.toml` or similar) and note the runtime and scripts.
2. Add a workflow that checks out the code, sets up the runtime with caching, installs, then runs lint, test and build.
3. Trigger it on push to `main` and on pull requests.
4. Push the branch and wait for the run.
5. Fix CI config until it passes, then open a pull request.

## Done when

- The workflow passes on the branch and runs on both push and pull request.

## Report back with

- The pull request link, the run result, and any step you couldn't make pass.
