# Level 19 → 20

## Concept
Using a SUID binary to read files as another user.

## Solution
```bash
ls -la                    # notice setuid bit (s) on bandit20-do
./bandit20-do whoami      # confirms it runs as bandit20
./bandit20-do cat /etc/bandit_pass/bandit20
```

## What I Learned
- SUID bit (`s`) makes a binary run as its owner, not the caller
- `ls -la` shows permissions — `rws` means SUID is set
- SUID binaries are a common privilege escalation vector
