# How to clean up github branches on your local machine!

Just:

```
git remote prune origin
git checkout main
git fetch -p && git branch -vv | awk '/: gone]/{print $1}' | xargs git branch -D
```
