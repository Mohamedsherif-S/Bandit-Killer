# Level 6 → 7

## Concept
Finding a file anywhere on the server by user, group, and size.

## Solution
```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

## What I Learned
- `find /` searches the entire filesystem
- `-user` and `-group` filter by ownership
- `2>/dev/null` hides permission denied errors
