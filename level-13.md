# Level 13 → 14

## Concept
Using an SSH private key to authenticate.

## Solution
```bash
# Copy the key to local machine
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .

# Connect using the key
ssh -i sshkey.private bandit14@localhost -p 2220
```

## What I Learned
- SSH supports key-based authentication with `-i keyfile`
- `scp` copies files over SSH
- Private keys must have permissions `chmod 600`
