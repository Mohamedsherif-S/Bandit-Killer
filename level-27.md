# Level 27 → 28

## Concept
Cloning a Git repository over SSH.

## Solution
```bash
mkdir /tmp/level27 && cd /tmp/level27
git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
cd repo
cat README
```

## What I Learned
- Git repos can be hosted over SSH
- `git clone ssh://user@host:port/path` clones a remote repo
- Password is found directly in README — simplest git level
