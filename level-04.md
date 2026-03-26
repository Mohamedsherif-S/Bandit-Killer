# Level 4 → 5

## Concept
Identifying file types to find human-readable content.

## Solution
```bash
file ./-file0*
cat ./-file07   # the one showing ASCII text
```

## What I Learned
- `file filename` shows the type of data inside a file
- Only ASCII/human-readable files contain readable passwords
