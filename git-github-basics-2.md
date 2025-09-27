# Git Rebase, Merge & Conflicts

## Rebase
Reapply commits on top of another base branch.

```bash
git rebase <branch>

----
Interactive Rebase
----

git rebase -i HEAD~4
# pick   → keep commit
# drop   → remove commit
# squash → combine commits (⚠️ Don't squash teammates’ commits!)

----
Useful Rebase Commands
----

git log --oneline --all
git pull origin master --rebase
git push origin master

----
Merge

Integrate changes from another branch.
----

git merge <source-branch>   # do this on destination branch
git merge -ff               # fast-forward merge
git merge --no-ff           # keep merge commit

----
Delete Branch
----

git branch -d <branch-name>   # safe delete
git branch -D <branch-name>   # force delete
git push origin --delete feature-1

----
Cherry-Pick

Apply a specific commit from another branch.
----

git cherry-pick <commit-hash>

----
Conflicts

Merge conflicts occur when changes overlap.

You must manually edit and resolve the conflicts, then:

git add <file>
git rebase --continue
# or
git commit

----
Collaboration Notes

Main branches (e.g. master or main) may be protected.

In such cases, you can’t push directly. Instead:

Fork the repo

Make changes

Open a Pull Request
