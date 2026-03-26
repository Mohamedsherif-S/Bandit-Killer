# Level 8 → 9

## Concept
Finding the only unique line in a file.

## Solution
```bash
sort data.txt | uniq -u
```

## What I Learned
- `uniq -u` prints only lines that appear exactly once
- `uniq` only works on adjacent duplicates — must `sort` first
- `uniq -c` shows count of repetitions
