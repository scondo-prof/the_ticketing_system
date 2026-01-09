# The Ticketing System

This repository is dedicated to tracking my current issues for projects across all repositories and life endeavors.

## About

This repository serves as a central hub for managing and organizing issues, tasks, and challenges that span across multiple projects, repositories, and personal initiatives. It provides a unified view of all ongoing work and areas that need attention.

## Discord Integration

This repository includes GitHub Actions workflows that automatically communicate issue actions to the `We Are In Hell` **Discord Server**. The workflows keep the team informed in real-time about issue activities and provide periodic updates.

### Workflows

#### Issue Event Integration (`github_issues_discord_integration.yml`)

This workflow monitors essential issue events and forwards them to the Discord server:

- Issue opened
- Issue closed
- Issue reopened
- Issue deleted

All these events are automatically communicated to the `We Are In Hell` **Discord Server** for team awareness.

#### Periodic Updates (`github-issues-discord-periodic-updates.yml`)

This workflow provides periodic updates about issues and can be triggered manually via `workflow_dispatch` or on a schedule (currently commented out). It uses the reusable workflow from `theToolKit` repository to send periodic status updates to Discord.
