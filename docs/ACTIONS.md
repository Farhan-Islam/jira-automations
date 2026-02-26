# Jira automation actions (reference)

Actions are what your rules do. They run in order; later steps can use smart values from earlier steps. Full list: [Jira automation actions](https://support.atlassian.com/cloud-automation/docs/jira-automation-actions).

## Work item actions

| Action | Purpose |
|--------|--------|
| **Assign work item** | Assign to user (list, round-robin, random, balanced, etc.). |
| **Create work item** | Create any work item type; set fields and copy attachments. |
| **Edit work item** | Set/change field values. |
| **Lookup work items** | JQL search (up to 100); use {{lookupIssues}} in later actions. |
| **Link work items** | Link to another issue. |

## Comments and notifications

| Action | Purpose |
|--------|--------|
| **Comment on work item** | Add comment; set visibility. |
| **Send customized email** | Branded email; plain/rich/HTML; attachments. |

## Logic and integrations

| Action | Purpose |
|--------|--------|
| **Create variable** | Define a smart value for the rest of the rule. |
| **Create lookup table** | Key to value map for same rule/branch. |
| **Send web request** | HTTP request; use response in later steps. |
| **Create branch in GitHub/Bitbucket/GitLab** | Requires connection. |
