# Level 22 → 23

## Concept
Reverse-engineering a cron script that generates a filename from a username.

## Solution
```bash
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh

# The script does:
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
# Use that hash as the filename in /tmp/
cat /tmp/<md5hash>
```

## What I Learned
- Cron scripts can generate dynamic filenames using hashes
- `md5sum` creates a hash, `cut` extracts just the hash value
- Reproducing the script's logic reveals where it stores the password
