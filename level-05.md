# Level 5 → 6

## Concept
Finding a file by specific properties (size).

## Solution
```bash
find ./ -size 1033c      # c = bytes
find ./ -size 1033c ! -executable
```

## What I Learned
- `find` can filter by size: `-size Nc` for bytes
- `! -executable` excludes executable files
- `ls -ls` shows detailed size, `ls -lh` shows human readable size
