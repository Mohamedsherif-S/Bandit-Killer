# Level 32 → 33

## Concept
Escaping an uppercase shell using special shell variables.

## The Trap
Every command typed gets converted to UPPERCASE before execution:
```
$ ls
sh: LS: command not found
```

## Solution
```bash
$0    # special variable — holds current shell name, not uppercased
# Now in a real shell running as bandit33 (SUID)
cat /etc/bandit_pass/bandit33
```

## What I Learned
- Shell special variables (`$0`, `$?`, `$$`) are expanded BEFORE filters run
- `$0` contains the path of the current shell
- Executing `$0` spawns a new interactive shell
- This was the final level — bandit33 just has a congratulations message!
