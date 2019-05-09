# Git Stash

How to retrieve the record of `git stash pop`.

1. Using `git stash apply ${commit}`.
2. If forget commit, using following command find out.

```shell
git log --graph --oneline $(git fsck | grep 'dangling commit' | awk '{print $3}')
```
