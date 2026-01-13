# The Ticketing System

This repository is dedicated to tracking my current issues for projects across all repositories and life endeavors.

## About

This repository serves as a central hub for managing and organizing issues, tasks, and challenges that span across multiple projects, repositories, and personal initiatives. It provides a unified view of all ongoing work and areas that need attention.

## Discord Integration

This repository includes GitHub Actions workflows that automatically communicate issue actions to the `We Are In Hell` **Discord Server**. The workflows keep the team informed in real-time about issue activities and provide periodic updates.

### Workflows

#### GitHub Issues to Discord Integration (`github-issues-discord-integration.yml`)

This workflow provides comprehensive Discord integration for issue management through a reusable workflow from the `theToolKit` repository. It consists of two main jobs:

**Issue Event Monitoring (`trigger-log-issue-details`):**

- Monitors and forwards essential issue events to the Discord server:
  - Issue opened
  - Issue closed
  - Issue reopened
  - Issue deleted
- Automatically triggered on issue events to communicate real-time updates to the `We Are In Hell` **Discord Server**.
- Uses the reusable workflow from `scondo-prof/theToolKit` repository to log issue details to Discord

**Periodic Updates (`trigger-periodic-issues-updates`):**

- Provides scheduled periodic updates about issues
- Can be triggered manually via `workflow_dispatch`
- Instead of using GitHub Actions' native `schedule` trigger, a scheduled AWS Lambda function triggers this workflow via `workflow_dispatch` to provide more reliable cron scheduling
- Uses the reusable workflow from `scondo-prof/theToolKit` repository to send periodic status updates to Discord

The workflow uses the reusable workflow located at `scondo-prof/theToolKit/.github/workflows/github-issues-discord-integration.yml@5-gh-periodic-issue-updates` and inherits all necessary secrets automatically.
