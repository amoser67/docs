# Git Cheat Sheet

### Backup Branches

##### Create backup branch:
1. `$ git checkout my-feature-branch`
2. `$ git checkout -b my-feature-branch-backup`
3. `$ git checkout my-feature-branch`
4. Do something risky.

##### Reset to backup branch:
1. `$ git checkout my-feature-branch`
2. `$ git reset --hard my-feature-branch-backup`
