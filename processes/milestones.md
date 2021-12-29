# Milestones

This document describes how Github milestones are used for the groupware repositories.

Milestones are handled differently for *apps* vs *libraries*.

## Apps

Apps use milestones for **tracking**, and not for *planning*. In other words, milestones are only assigned to issues or PRs that are *done* or planned to be done very soon.

### Milestone conventions

Github milestones should have the following format
* They start with a **v**, e.g. **v1.2.3**
* They have no due date assigned until we know when we'll release

Apps should have at least two milestones at any time

* Upcoming feature release: the next minor or major version, e.g. **v1.8.0** or **v4.0.0**
* Upcoming patch release: the next possible patch release for the last stable release, e.g. **v1.7.6**

### Bug reports (issue)

A bug report is a Github issue with the label `bug`. After triaging someone might or might not pick up the bug. Therefore we do not generally assign a milestone to it.

The rationale behind is that we don't always know when the next release is due. If we assign a milestone and the ticket doesn't get closed before the release, we'll have to reassign to the next milestone. History has shown that there will be some lower severity bugs that get reassigned all the time. This situation is both misleading and frustrating for the people affected by the bug, because assigning to a milestone gives a false promise.

### Bug fixes (pull request)

When a bug is fixed, we assign the milestone of the next feature release. If the fix qualifies for a backport, we create one and assign the milestone of the upcoming patch release.

### Feature requests (issue)

Feature requests are rarely assigned to a milestone. The exception is any feature that is planned as *must have* for a release. Anything that is optional or "done when it's done" remains unassigned.

### Feature implementations (pull request)

As with the feature requests, feature implementations are only assigned for implementations that are *done*. Drafts and proof of concepts should stay unassigned.

Once a pull request is assigned to a milestone we can assign the respective ticket as well.

## Libraries

We do not use milestones for libraries.