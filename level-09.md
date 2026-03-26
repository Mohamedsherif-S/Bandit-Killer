# Level 9 → 10

## Concept
Extracting human-readable strings from a binary file.

## Solution
```bash
strings data.txt | grep "=="
```

## What I Learned
- `strings` extracts printable text from any file (including binaries)
- Piping to `grep` narrows down the results
