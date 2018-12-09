Remove untracked files from current branch

to see will-be-deleted-files

```bash
git clean -n
```

to remove those files

```bash
git clean -f
```

to remove directories

```
git clean -fd
```

to remove ignored files

```
git clean -fX
```

to remove ignored and non-ignored files

```
git clean -fx
```

git magic

```
git update-index --skip-worktree
```

```
git update-index --skip-worktree src/config/auth-headers.js
```

Reverse

```
git update-index --no-skip-worktree <file>
```

GIT
Merge and Rebase:
https://www.atlassian.com/git/tutorials/merging-vs-rebasing
Interactive rebasing
 it offers complete control over the branch’s commit history
git rebase -i master
The golden rule of git rebase is to never use it on public branches.
So, before you run git rebase, always ask yourself, “Is anyone else looking at this branch?” If the answer is yes, take your hands off the keyboard and start thinking about a non-destructive way to make your changes (e.g., the git revert command)
gitk git bisect

.gitignore
https://www.atlassian.com/git/tutorials/gitignore
Git sees every file in your working copy as one of three things.

1. Tracked
2. Untracked
3. Ignored

Ignoring a previously committed file

```bash
$ echo debug.log >> .gitignore
$ git rm --cached debug.log
rm 'debug.log'
$ git commit -m "Start ignoring debug.log"
```

Undoing commits & changes

Aborting merge conflict

Git reset --hard HEAD

```
git reset
```

Reverting a rebase

```
git reflog
git reset —hard HEAD@{2}
```

Remove all your local git branches but keep master

```
git branch | grep -v "master" | xargs git branch -D
```

References

- [Git Clean](https://koukia.ca/how-to-remove-local-untracked-files-from-the-current-git-branch-571c6ce9b6b1)
