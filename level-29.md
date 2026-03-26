# Level 29 → 30

## Concept
Finding data hidden in a different Git branch.

## Solution
```bash
git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
cd repo
cat README.md          # says "no passwords in production!"
git branch -a          # list all branches including remote
git fetch origin
git checkout dev        # or: git checkout origin/dev
cat README.md
```

## What I Learned
- `main`/`master` is not the only branch — check them all
- `git branch -a` shows local AND remote branches
- `git fetch origin` downloads all remote branch info
- Development branches often contain data removed from production
