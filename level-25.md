# Level 25 → 26

## Concept
Escaping a restricted shell that runs `more` and exits.

## The Trap
`/usr/bin/showtext` is bandit26's shell. It runs:
```bash
exec more ~/text.txt
exit 0
```

## Solution
1. Check bandit26's shell: `cat /etc/passwd | grep bandit26`
2. **Shrink terminal window** to just 2-3 lines tall
3. SSH in with the private key — `more` is forced to pause
4. Press `v` to open vi
5. In vi: `:set shell=/bin/bash` then `:shell`

## What I Learned
- Terminal height affects whether `more` pauses or exits immediately
- `more` can open `vi` with the `v` key
- `vi` can spawn any shell via `:set shell=` and `:shell`
- Restricted shells are often escapable via text pagers
