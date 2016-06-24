---
published: true
title: Accepting all changes from another branch, preserving history
layout: post
---
Say you are up to date locally on a branch other then **dev**. To merge and accept all changes from upstream branch **dev**, you can:

    git.exe merge remotes/origin/dev
    git checkout --theirs *
    git add *
    git commit -m "Merged from dev"

Use gitk to verify that the history on the current branch is preserved:

    gitk