# AI Workflow Adviser / Optimiser Scenarios

This repository includes real-world GitHub Actions workflow examples created for **AI Awareness Week**. Each workflow simulates a distinct pattern or issue commonly found in CI/CD pipelines, and is linked with representative **AI prompts** for training or querying a Workflow Optimiser or Adviser.

---

## Workflow Files and AI Prompts

### [`workflow-scheduled-and-manual.yml`](.github/workflows/workflow-scheduled-and-manual.yml)

**Scenarios:**
- Scheduled Workflow (cron: every two hours)
- Manual Trigger

**AI Prompts:**
- Show workflows scheduled to run every two hours, daily or weekly.  
- List workflows that are triggered manually.

---

### [`workflow-push-fail-flaky.yml`](.github/workflows/workflow-push-fail-flaky.yml)

**Scenarios:**
- Push Trigger (to `master`)
- Constantly Failing Job
- Flaky Job

**AI Prompts:**
- Show workflows triggered on push to master branch.  
- Identify workflows that have failed in the last 10 runs.  
- Flag flaky workflows with unstable pass/fail rates.

---

### [`workflow-timeouts-and-long-jobs.yml`](.github/workflows/workflow-timeouts-and-long-jobs.yml)

**Scenarios:**
- Long-Running Job
- Timeout Case

**AI Prompts:**
- List jobs that consistently take more than 10 minutes.  
- Identify workflows that timed out.

---

### [`workflow-artifacts-errors-retry.yml`](.github/workflows/workflow-artifacts-errors-retry.yml)

**Scenarios:**
- Large Artifact Size / Upload Failures  
- Secrets or Permissions Errors  
- Too Many Steps / Redundant Steps  
- Repeated Retries or Reruns  
- Failing at Specific Steps

**AI Prompts:**
- List workflows generating artifacts over 500MB or having upload failures.  
- Show jobs failing due to secrets or permission issues.  
- Show workflows with over 30 steps or repeated commands.  
- Find workflows rerun more than 3 times in the past week.  
- Find workflows that fail repeatedly at the same step.

---

### [`do-not-trigger.yml`](.github/workflows/do-not-trigger.yml)

**Scenarios:**
- Never Triggered / Obsolete Workflows  
- Inconsistent Duration (based on historical logs)

**AI Prompts:**
- List workflows that haven’t been triggered in the last 90 days.  
- Show jobs with inconsistent execution times across runs.

---

### [`needs-optimization.yml`](.github/workflows/needs-optimization.yml)

**Scenarios:**
- Redundant Serial Execution 
- Skipped Job in Every Run

**AI Prompts:**
- Suggest jobs that could run in parallel instead of serially.  
- Show jobs skipped in the last 10 runs.
- Suggest redundant jobs or steps that don't add value.

---

### [`concurrency.yaml`](.github/workflows/concurrency.yaml)

**Scenarios:**
- Frequent Job Cancellations Due to Concurrency
- Overly Restrictive Concurrency Settings
- Critical Steps Canceled Mid-Execution

**AI Prompts:**
- Show how many jobs were canceled in the last 10 runs due to concurrency.
- Identify critical steps most often skipped due to canceled jobs.

---

### [`flake-retry.yaml`](.github/workflows/flake-retry.yaml)

**Scenarios:**
- Redundant Retry Logic for Non-Deterministic Failures
- Retry Job Succeeds Randomly Without Fixing Root Cause
- Wasted Resources on Retrying Flaky Steps

**AI Prompts:**
- Show how often retry-if-fail succeeded after first-try failed.
- Suggest whether a built-in retry strategy would be more efficient than a separate job.
- Identify flaky steps that frequently fail and succeed inconsistently.

---


### [`flaky-expo.yaml`](.github/workflows/flaky-expo.yaml)

**Scenarios:**
- Inefficient Retry with Fixed Backoff Regardless of Failure Type
- Masked Flakiness Without Root Cause Resolution
- Excessive Delay Causing Long CI Times

**AI Prompts:**
- Show how often all retries are exhausted in the flaky-backoff job.
- Suggest smarter retry conditions instead of uniform exponential backoff.
- Identify if the same step fails repeatedly even after retries, indicating deeper flakiness.

---


### [`flaky-inline-retry.yaml`](.github/workflows/flaky-inline-retry.yaml)

**Scenarios:**
- Lack of Visibility Into Which Attempt Succeeds
- Manual Retry Logic Duplicated Across Jobs
- Retry Masking Infrastructure or Dependency Issues

**AI Prompts:**
- Highlight steps where success consistently happens only on the last attempt.
- Detect patterns of similar retry logic used across multiple workflows.
- Recommend built-in GitHub Actions retry strategies or reusable actions for handling flakiness.
- Identify if flakiness correlates with specific times, runners, or external dependencies.

---

### [`flaky-jitter.yaml`](.github/workflows/flaky-jitter.yaml)

**Scenarios:**
- Unpredictable Build Times Due to Random Jitter
- Retry Logic Adds Variance Without Addressing Root Cause
- Hidden Instability Behind Successful Final Attempt

**AI Prompts:**
- Show how jitter impacts average retry duration across runs.
- Identify if adding jitter improves success rate compared to fixed or exponential delays.
- Suggest standardizing retry strategies across workflows for consistency and traceability.
- Detect steps where retries succeed frequently only after multiple jittered delays.

---























