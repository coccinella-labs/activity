# Tracking Workflow

[![Release](https://img.shields.io/github/v/release/libnudget/activity?logo=github&label=latest)](https://github.com/libnudget/activity/releases)

A reusable GitHub Action for tracking project activity in a central issue.

## Usage

### Option 1: Using repository variable (recommended)

1. Set `TRACKING_ISSUE_NUMBER` in **Settings > Secrets and variables > Variables**
2. Add this to your workflow:

```yaml
jobs:
  track:
    uses: bniladridas/tracking-workflow/.github/workflows/tracking.yml@main
```

### Option 2: Passing as input

```yaml
jobs:
  track:
    uses: bniladridas/tracking-workflow/.github/workflows/tracking.yml@main
    with:
      tracking_issue_number: 113
```

## How it works

- Triggers when issues or PRs are opened, closed, or reopened
- Posts an automated comment to the tracking issue with:
  - Type (Issue or PR)
  - Number and title
  - Status and action
  - Date created

The input parameter takes priority over the variable if both are set.
