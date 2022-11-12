---
layout: post
title: "Git Cheat sheet"
date: 2014-09-15 22:21:48 +0100
comments: true
published: true
categories: blog
---

Git commands that I always forget but find useful:


```bash
# Recover a file:
git checkout <previous-commit-hash> <file_path>

# Ignore changes to certain files:
git update-index --assume-unchanged config/database.yml

# Take commit from another branch:
git cherry-pick <commit reference>

# Delete multiple branches starting with some string:
git branch -D `git for-each-ref --format="%(refname:short)" refs/heads/some_string\*`

# Delete all branches merged with master
git branch --merged | egrep -v '(^\*|master)' | xargs git branch -d

# List branches in order of which most recent commit
git for-each-ref --sort=-committerdate refs/heads/
```


I tend to alias things so when on another machine it's handy!