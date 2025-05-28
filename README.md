# 🧠 AI Workflow Adviser / Optimiser Scenarios

This repository includes real-world GitHub Actions workflow examples created for **AI Awareness Week**. Each workflow simulates a distinct pattern or issue commonly found in CI/CD pipelines, and is linked with representative **AI prompts** for training or querying a Workflow Optimiser or Adviser.

---

## 📁 Workflow Files and AI Prompts

### [`workflow-scheduled-and-manual.yml`](.github/workflows/workflow-scheduled-and-manual.yml)

**Scenarios:**
- Scheduled Workflow (cron: daily)
- Manual Trigger

**AI Prompts:**
- Show workflows scheduled to run daily or weekly.  
- List workflows that are triggered manually.

---

### [`workflow-push-fail-flaky.yml`](.github/workflows/workflow-push-fail-flaky.yml)

**Scenarios:**
- Push Trigger (to `main`)
- Constantly Failing Job
- Flaky Job

**AI Prompts:**
- Show workflows triggered on push to main branch.  
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
