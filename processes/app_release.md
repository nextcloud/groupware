## App release commands

---
### Below you will find step by step how to do a release for groupware apps

1. Change directory to the app directory and make sure your environment is clean with git status

2. git checkout stablex.x (patch release) or master/main (major/minor release) (this is the branch we want to release)

3. git pull to have the latest changes

4. git log v1.2.3..HEAD --oneline - this shows all the commits from version v1.2.3 (last release) to HEAD (latest unreleased commit)

    4.1 To ignore the "Merge .." commit you do git log v1.2.3..HEAD --oneline | grep -v "Merge "

5. The commits will be shown, and then we can create a change log with the commits that are shown.

6. We change the version on info.xml, package.json and package-lock.json

    6.1 Tip - Expected number of changed files is 4

7. git checkout -b release/x.x.x to create the release branch

8. git add, git commit (add the version as message) and then we can

9. git push origin release/x.x.x and open a new PR against the target branch (stablex.xx or master/main)

10. Once merged, git pull the latest changes

11. git tag vx.x.x

12. git push origin stablex.x --tags (this means we push the commit + tags)

13. We should also push it to the release git push release stablex.x --tags

14. Then we go to the release's repository tags page, e.g. https://github.com/nextcloud-releases/mail/tags

    14.1 On this draft we add the tag we created, add the change log and publish the release

    14.2 Wait a few minutes for the automation to build the app, add the app .tar.gz to the release and push it to the app store

15. Open the app's main repo and close the vx.y.z milestone

16. Create a milestone for the next patch version

17. If the release was for patch version, forward-port the changelog to master/main
