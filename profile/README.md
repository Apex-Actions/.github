# Apex Actions

**Your GitHub Actions workflows, running faster and for less — without changing a line of YAML.**

Apex Actions is a drop-in replacement for GitHub-hosted runners. It runs your existing `.github/workflows/*.yml` files as they are, reports back to GitHub the way you already expect — check runs, annotations, required status checks — and swaps metered runner minutes for fast, dedicated compute on a simple flat plan.

[apexactions.com](https://apexactions.com)

---

## Why Apex Actions

CI is part of every change your team ships, and GitHub-hosted runners make you pay for it twice: once in per-minute billing that climbs with every larger machine, and again in time spent waiting in queues and debugging runs you can't reproduce.

Apex Actions fixes both without asking you to migrate. **Compatibility comes first.** A conformance suite continuously checks Apex Actions against GitHub's documented behaviour, so your workflows run on day one. Everything else is built on top of that.

---

## Features

### Your workflows, unchanged

Same YAML, same marketplace actions, same check runs. Triggers, matrices, `${{ }}` expressions, reusable workflows, composite and JavaScript actions, caches and artifacts all carry over. Installing the GitHub App is the only change GitHub sees.

### Jobs start in seconds

Capacity follows your queue. A push becomes a running job with no queue position and no warm-up, and larger machines are there when you need them.

### One subscription, not a meter

A flat monthly plan with larger runners included, instead of paying per minute and per machine size. Teams typically spend about half of what they pay for GitHub-hosted minutes.

### Run it before you push

The engine that plans your CI also runs on your laptop and in your editor. Validate workflows as you type, and run a whole job locally with `apex run`.

### Know why every run happened

A clear verdict for every workflow — including the ones that *didn't* run, and why. Flaky tests are flagged automatically, every step is timed against its own history, and any failure comes with a one-line local repro.

### Secure by default

Short-lived OIDC credentials instead of long-lived keys, protected environments with required reviewers, clearly resolved permissions, and encrypted secrets that never reach a log.

### A dashboard built for CI

Browse repositories and runs, trigger `workflow_dispatch` workflows from typed forms, follow live logs, explore each run as a job graph, re-run failures, and manage secrets and variables — all behind GitHub sign-in.

---

## Getting started

1. **Sign up** at [apexactions.com](https://apexactions.com) and sign in with GitHub.
2. **Install the Apex Actions GitHub App** on the organization or repositories you want to run.
3. **Push a commit.** Your existing workflows run on Apex Actions and report back to the pull request as usual — no YAML changes required.
4. **Watch it run** in the Apex Actions dashboard, with live logs and a full history for every job.

### Try it locally

Install the `apex` CLI (see [apexactions.com](https://apexactions.com) for instructions), then from any repository:

```bash
# Check your workflow files for errors
apex validate .github/workflows/*.yml

# Run a workflow job on your machine (requires Docker)
apex run
```

---

## Get in touch

Questions, feedback or a workflow that doesn't behave the way it does on GitHub? Visit [apexactions.com](https://apexactions.com) — compatibility reports are always welcome.
