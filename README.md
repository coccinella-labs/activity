# Tracking Workflow

A reusable GitHub Action for tracking project activity in a central issue.

## Usage

Add this to your workflow:

```yaml
jobs:
  track:
    uses: bniladridas/tracking-workflow/.github/workflows/tracking.yml@main
    with:
      tracking_issue_number: 113
```

Replace `113` with your tracking issue number.

## How it works

- Triggers when issues or PRs are opened, closed, or reopened
- Posts an automated comment to the specified tracking issue with:
  - Type (Issue or PR)
  - Number and title
  - Status and action
  - Date created
