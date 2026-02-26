# Jira automation best practices

Based on Atlassian create and edit automation rules docs.

## Creating rules

- From template: Space settings, Automation, Create rule, Use a template.
- With Rovo: Describe trigger and action; preview and edit.
- From scratch: Pick trigger, add conditions, add actions. You must add at least one action.

Rule components run in order. Keep dependencies in mind (e.g. Lookup work items before using lookupIssues).

## Rule details

Set Name, Description, Scope, Owner, Actor, Notify on error before enabling.

## Testing

- Use Manual trigger to test on a single issue.
- Check the automation audit log after enabling to confirm runs and debug failures.

## Documentation

- Document each rule in this repo under rules/.
- Use Import/Export if your Jira plan supports it and store exports in version control.
