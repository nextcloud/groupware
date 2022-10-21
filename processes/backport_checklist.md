# Checklist for Backporting Pull Requests

1. Determine which Nextcloud versions are supported by visiting the [maintenance schedule](https://github.com/nextcloud/server/wiki/Maintenance-and-Release-Schedule).
2. Determine the branch of the app corresponding to the supported Nextcloud versions.
    1. Go to the app store page of the app, e.g. [Mail](https://apps.nextcloud.com/apps/mail).
    2. Scroll down to `Downloads`.
    3. Have a look at the version table and take note of our app version.
    4. Derive the branch name by using the following pattern: `stable{MAJOR}.{MINOR}` (replace
    `{MAJOR}` and `{MINOR}` with their respective versions)
3. Instruct the backport bot by commenting on the pull request with `/backport to stableX.X`.
4. Done! Now, wait for the bot to do its work. It will automatically open a new pull request with
the backport.
5. *Optional:* In some cases the backport bot will fail and won't crate a PR.
Instead, it will leave a comment stating the error.
You have to cherry pick the commits and create a new PR manually in those cases.

### Example

Let's assume that Nextcloud 23 - 25 are supported according to the maintenance schedule and the app
store contains the following table:

|              |       |
| ------------ | ----- |
| Nextcloud 25 | 2.0.3 |
| Nextcloud 24 | 1.14.1|
| Nextcloud 23 | 1.14.1|

That means that we need to backport to `stable2.0` and `stable1.14`.

## Exceptions

These rules apply in most cases.
However, there are some exceptions to the rules.

### Exception: Recent features

If a feature is fairly new it might not have to be backported to all supported stable branches.
For example, a fix for a feature added in v2.1 has to be backported to `stable2.1` and all branches
after that (e.g. `stable3.0`).

When in doubt, you can search for the PR implementing a feature and consult its milestone.
The milestone is named after the version a feature was introduced.
Bug reports also often contain the version of an app on which the bug occurred.
Just check the issue you fixed and look for the app version.
