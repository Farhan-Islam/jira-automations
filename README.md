# Jira Automations

A single place for all Jira automation rules, documentation, and templates. Use this repo to document, version, and share your automations across projects and teams.

## What's in this repo

| Path | Purpose |
|------|--------|
| **`docs/`** | Jira automation reference: triggers, actions, and practices |
| **`rules/`** | Your automation rules: one doc per rule (or group) for backup and reuse |
| **`templates/`** | Reusable rule descriptions and copy-paste snippets for Jira UI |

## Quick links (official Jira docs)

- [Create and edit automation rules](https://support.atlassian.com/cloud-automation/docs/create-and-edit-jira-automation-rules)
- [Jira automation triggers](https://support.atlassian.com/cloud-automation/docs/jira-automation-triggers)
- [Jira automation actions](https://support.atlassian.com/cloud-automation/docs/jira-automation-actions)
- [Automation rule examples and use cases](https://support.atlassian.com/automation/kb/automation-rule-examples-and-use-cases/)
- [Use automation components in a rule](https://support.atlassian.com/cloud-automation/docs/what-are-automation-rules)

## Rule structure (reminder)

Every Jira automation rule has three parts:

1. **Trigger** – When the rule runs (e.g. issue created, field changed, scheduled, webhook).
2. **Conditions** – Optional filters so actions only run when criteria are met.
3. **Actions** – What the rule does (e.g. edit issue, assign, comment, send email, create branch).

Rules run **top to bottom**; order matters. Use the **automation audit log** to confirm runs and debug failures.

## How to add a new automation

1. Create the rule in Jira (Space → **More actions** → **Space settings** → **Automation**), using a template, Rovo, or from scratch.
2. In this repo, add a file under `rules/` (e.g. `rules/assign-on-triage.md`) using the [rule template](templates/rule-template.md): name, trigger, conditions, actions, scope, and any notes.
3. Optionally add reusable text (e.g. comment bodies, email copy) under `templates/` for easy copy-paste into Jira.
4. Commit and push so the rule is documented and versioned.

## Clone and open

```bash
git clone https://github.com/Farhan-Islam/jira-automations.git
cd jira-automations
```

---

*Jira Cloud automations are configured in the product UI; this repo is for documentation, backup, and reuse, not for deploying rules via code.*
