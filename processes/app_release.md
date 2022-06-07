## App release commands
#### Below you will find step by step how to do a release for groupware apps
## Preparation 
1. Change directory to the app directory and make sure your environment is clean with `git status`
2. Check if you have the remote release by running `git remote -v` if that points to `git@github.com:nextcloud-releases/AppName.git`, you're good
3. If you don't see that in the list, do `git remote add release git@github.com:nextcloud-releases/AppName.git`
## Process of the release
4. For patch release do `git checkout stablex.x` (the latest stable version you have) or master/main for major/minor release (this is the branch we want to release)

5. `git pull` to have the latest changes

6. `git log v1.2.3..HEAD --oneline` - this shows all the commits from version v1.2.3 (last release) to HEAD (latest unreleased commit)

    6.1 To ignore the "Merge .." commit you do `git log v1.2.3..HEAD --oneline | grep -v "Merge "`

7. The commits will be shown, and then we can create a change log with the commits that are shown.

8. We change the version on `info.xml`, `package.json` and `package-lock.json`

    8.1 Tip - Expected number of changed files is 4

9. `git checkout -b release/x.x.x` to create the release branch

10. `git add`, `git commit` (add the version as message) and then we can

11. `git push origin release/x.x.x` and open a new PR against the target branch (stablex.xx or master/main)

12. Once merged, switch back to the target branch and `git pull` the latest changes

13. `git tag vx.x.x`

14. `git push origin stablex.x vx.x.x` (this means we push the commit + tag)
15. Run `git push release stablex.x vx.x.x` to push it also to the release remote 

    15.1 In case you're releasing from `main`, only push the tag to the release remote: `git push release vx.xx.xx`
16. If the case is a minor or major version, you need to branch off this minor or major release: `git checkout -b  stablex.x` then do `git push origin stablex.x`

17. We go to the release's repository tags page, e.g. https://github.com/nextcloud-releases/mail/tags

    17.1 On the draft we add the tag we created, add the change log and publish the release

    17.2 Wait a few minutes for the automation to build the app
    
    17.3 The package will be automatically built and attached to the new release

18. Open the app's main repo and close the vx.y.z milestone (Issues -> Milestones in the Right Upper Corner)
19. Create a milestone for the next patch/major/minor version
20. After branch off, you need to create a new separate PR against main to change the `info.xml` version to x.x.0-alpha.1, so add the suffix `-alpha.1` to your branch off release version
21. If the release was for patch version, forward-port the changelog to master/main. Open a PR against main with the section of the changelog of your current release. Push it and after merge you're done.
