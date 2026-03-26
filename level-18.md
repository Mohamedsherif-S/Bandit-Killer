# Level 18 → 19

## Concept
Running a command via SSH without an interactive shell (`.bashrc` logs you out).

## Solution
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```

## What I Learned
- SSH can run a single command: `ssh user@host command`
- Useful when `.bashrc` or `.bash_logout` causes immediate logout
