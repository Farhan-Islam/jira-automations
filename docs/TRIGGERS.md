# Jira automation triggers (reference)

Triggers start your rules. They listen for events in Jira (and connected tools) and can be narrowed with conditions. Below is a concise reference; full details: [Jira automation triggers](https://support.atlassian.com/cloud-automation/docs/jira-automation-triggers).

## General triggers (all Jira products)

| Trigger | When it runs | Smart values |
|--------|----------------|--------------|
| **Field value changed** | Any system/custom field changes (create, edit, transition, assign). Supports regex and change type. | `{{fieldChange}}` |
| **Form attached** | Form attached to work item (manual or via Add form / Copy form API). Space-specific. | — |
| **Form submitted** | Form(s) on a work item submitted. Can target specific form(s). Space-specific. | — |
| **Incoming webhook** | HTTP POST to your rule webhook URL. | `{{webhookData}}` |
| **Work item assigned** | Assignee changes. | `{{assignee}}` |
| **Work item commented** | New comment added (filter by comment type). | `{{comment}}` |
| **Work item created** | Work item is created. | `{{issue}}` |
| **Work item transitioned** | Status transition. | `{{issue}}`, `{{changelog}}` |
| **Work item updated** | Work item details updated. | `{{issue}}` |
| **Manual trigger from work item** | User runs the rule from Actions. Good for testing. | `{{issue}}` |
| **Scheduled** | Cron or fixed interval; optional JQL. | `{{issue}}` |

## DevOps triggers (Jira Cloud + SCM/CI)

| Trigger | When it runs |
|--------|----------------|
| **Branch created** | Branch created in connected repo. |
| **Pull request created / declined / merged** | PR lifecycle. |
| **Build/Deployment** | Build or deployment status events. |

## Best practices

- Use conditions on the trigger to limit which events run the rule.
- Prefer Work item transitioned for status changes; Work item updated for other edits.
- Scheduled rules that fail 10 times in a row are auto-disabled.
