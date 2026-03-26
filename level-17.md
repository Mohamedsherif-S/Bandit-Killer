# Level 17 → 18

## Concept
Finding the difference between two files.

## Solution
```bash
diff passwords.old passwords.new
```

## What I Learned
- `diff file1 file2` shows lines that differ
- Lines with `<` are in file1 only, `>` are in file2 only
- The changed line in passwords.new is the new password
