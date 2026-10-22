# Jira Add Comment Action

Adds a plain-text comment to a Jira Cloud issue. The action converts the text to Atlassian Document Format before calling Jira.

## Example

```yaml
- name: Add workflow traceability
  id: add-comment
  uses: https://bitbucket.org/adp-uat/adp-jira-add-comment@v1.0.0
  with:
    jira-url: https://adp-uat.atlassian.net
    jira-email: ${{ secrets.JIRA_EMAIL }}
    jira-api-token: ${{ secrets.JIRA_API_TOKEN }}
    issue-key: ${{ steps.create-story.outputs.issue-key }}
    comment: Created by CloudBees Unify workflow run ${{ cloudbees.run_id }}.
```

## Output

```text
comment-id
```

