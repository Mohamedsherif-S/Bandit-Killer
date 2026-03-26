# Level 28 → 29

## Concept
Finding deleted data in Git commit history.

## Solution
```bash
git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
cd repo
cat README.md          # password is hidden as xxxxxxx
git log                # see commit history
git log -p             # shows full diff of every commit
# Find the commit where password was removed (lines starting with -)
```

## What I Learned
- Git never truly deletes data — it stays in commit history
- `git log -p` shows all additions (+) and deletions (-) per commit
- `git show HASH` shows a specific commit's changes
- Sensitive data committed to git is permanently exposed
