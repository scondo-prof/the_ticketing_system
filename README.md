# The Ticketing System

This repository is dedicated to tracking my current issues for projects across all repositories and life endeavors.

## About

This repository serves as a central hub for managing and organizing issues, tasks, and challenges that span across multiple projects, repositories, and personal initiatives. It provides a unified view of all ongoing work and areas that need attention.

## Discord Integration

This repository includes a GitHub Actions workflow that automatically communicates issue actions to the `We Are In Hell` **Discord Server**. Whenever issues are created, updated, or have any status changes, the workflow will send notifications to the Discord server to keep the team informed in real-time.

The integration workflow (`github_issues_discord_integration.yml`) monitors all issue-related events and forwards them to the Discord server for seamless collaboration and visibility.

## Workflow

The workflow is triggered by the following issue events:

- Issue opened, closed, reopened
- Issue edited or deleted
- Issue comments (created, edited, deleted)
- Issue assignments and labels
- Milestone updates
- And more...

All these events are automatically communicated to the `We Are In Hell` **Discord Server** for team awareness.
