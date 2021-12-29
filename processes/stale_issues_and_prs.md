# Stale issues and PRs

It's not always easy to keep an overview of the bug reports and features in our issue trackers. When a maintainer initially sees a new issue it can be easy to classify it as actionable or wontfix. But sometimes we have to keep tickets open until we have more info, know if the bug affects more than one user, wait for external changes and also see if a requested feature interests more than one person.

Those tickets will then either receive more activity, e.g. because the requested info is provided or more people chime in to report their findings. In that case the maintainer can relabel the issue from `0. to triage` to `1. to develop`.

Other tickets might never get updated again. This happens for bug reports that are incomplete or not reproducible. Also feature requests tend to be silent if there is little to no interest by other people.

Automation will comment on those stale issues, so that the maintainer can have a second look. Then we can decide if the ticket is valid and should get relabeled, or closed otherwise.

In the rare case that a ticket is not updated by anyone we will close it after a long grace period. This still doesn't mean the ticket can't be reconsidered. Maintainers can reopen at any time and relabel accordingly.

## Automation

* Runs daily
* Tickets
  * Stale after three weeks
    * Tickets with a status label (to develop, developing, review) are not considered stale. It's only unlabeled ones and the ones to triage
    * A comment is left for the main repo maintainer to please triage the ticket
  * Closed after five weeks of no activity
* Pull requests
  * Stale after a week
    * A comment is left for the main repo maintainer to please have a look
  * Closed after half a year of no activity

```yml
name: 'Close stale issues and PRs'
on:
  workflow_dispatch:
  schedule:
    - cron: '0 3 * * *'

jobs:
  stale:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/stale@v4
        with:
          # Issues
          days-before-issue-stale: 21
          days-before-issue-close: 35
          stale-issue-label: 'stale'
          stale-issue-message: 'This ticket had no activity recently. @ChristophWurst please adjust the labels if this ticket should stay open and close it otherwise. [Learn more about the stale process](https://github.com/nextcloud/groupware/blob/main/processes/stale_issues_and_prs.md)'
          close-issue-message: 'This ticket has had no activity for a while, so we are closing it. If this is due to information missing on a bug report, we can re-open the ticket once the info is provided. [Learn more about the stale process](https://github.com/nextcloud/groupware/blob/main/processes/stale_issues_and_prs.md)'
          exempt-issue-labels: '1. to develop,2. developing,3. to review,4. to release'
          # PRs
          days-before-pr-stale: 7
          days-before-pr-close: 180
          stale-pr-label: 'stale'
          stale-pr-message: 'This pull request needs attention. @ChristophWurst have a look please! [Learn more about the stale process](https://github.com/nextcloud/groupware/blob/main/processes/stale_issues_and_prs.md)'
          close-pr-message: 'This pull request has had no activity for a while, so we are closing it. If the changes are still applicable and should be integrated, please get in contact with the maintainers, they can reopen. [Learn more about the stale process](https://github.com/nextcloud/groupware/blob/main/processes/stale_issues_and_prs.md)'
          # Other config
          enable-statistics: true
```
