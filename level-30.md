# Level 30 → 31

## Concept
Finding data stored in a Git tag.

## Solution
```bash
git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
cd repo
cat README.md          # just an empty file
git log                # nothing useful
git tag                # lists all tags
git show <tagname>     # reveals the password
```

## What I Learned
- Git tags mark specific points in history (e.g. v1.0 releases)
- Tags can store arbitrary data, not just version markers
- `git tag` lists all tags, `git show tagname` reads the tag content
