# Structuring a Task Ticket

Clear and concise tickets are easier to understand, track and execute. This page shall help find a good structure for Github tickets that are used to track tasks and work packages.

## Ground Work: What Is the Task About?

Describe the problem and the solution. If it's a feature, write a user story and include the problem and solution from a user's perspective.

A clear user story helps form acceptance criteria. It also helps others test your work when it's ready for review and acts as a blueprint for the user documentation.

## Deep Dive: How Could This Be Solved?

Get acquainted with the problem. Look at reference implementations. Study RFCs. Exchange ideas with colleagues.

Once you have a rough idea of a solution, write it down. Iterate on the implementation idea as the feature shapes up. The text helps reviewers and testers understand the changes better.

Write down useful links (like RFCs) for later reference.

## Breakdown: Small Changes are Good Changes

Huge PRs are tough for everyone involved. They need more time to get merged, therefore are more likely to cause conflicts. They are also harder to review and test. If something goes wrong, it's not always trivial to revert them. Try to break your work into iterative chunks whenever possible. The granularity should be at a level where the individual chunks form a meaningful change and, ideally, are releasable.

An example of a meaningful iteration is a minimalist MVP as first iteration. The MVP works but has only the most crucial features. Anything else is left out. These optional but planned features are added in follow-ups. Take one step after the other.

Another example is required refactoring before your changes can be made. Do them in a separate PR. Apply your changes to the main branch after the refactoring merge.

In some cases it can make sense to add the back-end parts of a feature first if they have no influence on other features. These changes are only tested with automated tests, not the front-end counterpart. The situation is not ideal, because dead code lives in the main branch until the counterparts are done.

Last but not least, documentation should be seen as a part of feature development.

### Scoping: Required, Optional or Must Not?

Brainstorming about a feature can lead to wonderful ideas. Yet some of them might be impossible to do with current technology, are blocked by external factors, require resources currently not available or do not fit the project goals. A ticket should clearly say which parts of a feature are required, nice to have or not planned.

### Work packages: One Ticket Per Change

Every chunk of a task should have its own ticket. The ticket can be tracked on a project board and has a clear open/closed state and labels. The work package tickets can be feature requests or bug reports. They should be created in the repository with most relevance. E.g. if a Calendar task requires enhancements of the CalDAV backend, create a feature request in the server repository.

All work packages have to be listed in the task ticket: required ones become a checklist, optional ones become a simple bullet point list. The task ticket stays open until all required work packages have been done and their tickets are closed.

## Example Ticket Structure

```md
## Feature Request

As a user, I want to x. It is tedious when the y. Offer a way to z.

## Implementation

RFC1234 covers how IMAP clients can z …

* Front-end handles x (already there)
* Move y handling from synchronous operation to cron job
* Add z to front-end, store state in browser

## Work packages
- [x] https://github.com/nextcloud/mail/issues/100
- [ ] https://github.com/nextcloud/nextcloud-vue/issues/10
- [ ] https://github.com/nextcloud/mail/issues/101
- [ ] https://github.com/nextcloud/server/5000
- [ ] https://github.com/nextcloud/documentation/321

## Follow-ups
- https://github.com/nextcloud/mail/issues/103
- https://github.com/nextcloud/mail/issues/104

## Out of scope
- Foo
- Bar
```
