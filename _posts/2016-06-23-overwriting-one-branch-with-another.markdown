---
published: true
title: Overwriting one branch with another
layout: post
---
Say you have upstream changes on one branch and you to overwrite changes on different branch.

If the local branch is test and you are currently on that branch, the command to overwrite from branch dev would be

git reset --hard origin/dev

This leaves you out of sync with the upstream of branch test, so to resolve this you can do:

git push origin test --force

THIS WILL TOTALLY DELETE THE HISTORY OF THE UPSTREAM BRANCH

As usual, --force indicates a destructive operation and should be used with caution