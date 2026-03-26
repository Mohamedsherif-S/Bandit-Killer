# Level 1 → 2

## Concept
Reading a file with a dashed filename (`-`).

## Problem
`cat -` doesn't work because `-` means stdin to most commands.

## Solution
```bash
cat < -
# or
cat ./-
```

## What I Learned
- `-` is interpreted as stdin by most commands
- Use `./` prefix or input redirection `<` to read dashed filenames
