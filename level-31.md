# Level 31 → 32

## Concept
Pushing a file to a remote Git repository, bypassing .gitignore.

## Solution
```bash
git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
cd repo
cat README.md          # instructions: push key.txt with "May I come in?"
cat .gitignore         # blocks *.txt files

echo "May I come in?" > key.txt
git add -f key.txt     # -f forces add, bypasses .gitignore
git commit -m "add key"
git push origin master
# Password appears in the push output
```

## What I Learned
- `.gitignore` prevents files from being tracked automatically
- `git add -f` force-adds a file even if it matches `.gitignore`
- Server-side git hooks can validate pushes and return data
