# Clean-up of Groupware repo milestones, labels and automation

## Attendees

* Anna
* Christoph
* Thomas

## Notes

* Overview ticket https://github.com/nextcloud/groupware/issues/9
* We went through Calendar milestones
  + Closed old releases that won't happen (2.4.1 mainly)
  + Unassigned any tickets and PRs that are not planned from milestones
* We went through Calendar labels
  + Compared to the documented ones and what is used in Mail
  + Dropped/renamed some labels
* Same procedure for Contacts
* We assigned CalDAV/CardDAV labels to `feature: dav` tickets in server to distinguish generic DAV from Groupware DAV

## Actionable items
* Dev docs labels need an update, two label pages should be unified
* Repo labels should follow the documented ones, have the same name, description and color
* We should formalize the bug triage process, how to assign labels and so on
* A link from this repo's readme to *dav bugs could be useful as quick reference to bugs relevant for us
* Revise *good first issue* tickets
  + Quality > quantity
  + We should aim for a few good tickets in each repo
  + Define a process so we always make sure those tickets exist
* Look into automation
  + Probably can use Github actions
  + Do automation in two steps, so we first warn, then we close
  + Phrase the close texts nicely, ideally point to some docs of the process
  + Look into promoting the automations orga-wide, though they will likely not be applicable in all repos in the same way
