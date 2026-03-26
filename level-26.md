# Level 26 → 27

## Concept
Using a SUID binary (same concept as level 19).

## Solution
```bash
ls -la ~
./bandit27-do cat /etc/bandit_pass/bandit27
```

## What I Learned
- SUID binary `bandit27-do` runs as bandit27
- Same privilege escalation pattern as level 19
- Always check home directory for interesting binaries
