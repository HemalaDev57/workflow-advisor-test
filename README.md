AI Workflow Scenarios and Prompts
This repository contains real-world GitHub Actions workflows designed for evaluation by an AI Workflow Adviser / Optimiser. Each workflow simulates different issues or patterns and is linked below along with relevant AI prompt examples.

Workflow Files
workflow-scheduled-and-manual.yml

Scenarios:
Scheduled Workflow (cron: daily)
Manual Trigger

AI Prompts:

Show workflows scheduled to run daily or weekly.

List workflows that are triggered manually.

workflow-push-fail-flaky.yml
Scenarios:

Push Trigger (to main)

Constantly Failing Job

Flaky Job

AI Prompts:

Show workflows triggered on push to main branch.

Identify workflows that have failed in the last 10 runs.

Flag flaky workflows with unstable pass/fail rates.

workflow-timeouts-and-long-jobs.yml
Scenarios:

Long-Running Job

Timeout Case

AI Prompts:

List jobs that consistently take more than 10 minutes.

Identify workflows that timed out.

workflow-artifacts-errors-retry.yml
Scenarios:

Large Artifact Size / Upload Failures

Secrets or Permissions Errors

Too Many Steps / Redundant Steps

Repeated Reruns

Failing at Specific Steps

AI Prompts:

List workflows generating artifacts over 500MB or having upload failures.

Show jobs failing due to secrets or permission issues.

Show workflows with over 30 steps or repeated commands.

Find workflows rerun more than 3 times in the past week.

Find workflows that fail repeatedly at the same step.

obsolete.yml (Optional)
Scenarios:

Never Triggered / Obsolete Workflows

Inconsistent Duration (implied via logs/metrics)

AI Prompts:

List workflows that haven’t been triggered in the last 90 days.

Show jobs with inconsistent execution times across runs.

