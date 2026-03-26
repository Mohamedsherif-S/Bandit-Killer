# Level 21 → 22

## Concept
Reading cron jobs to find scheduled scripts.

## Solution
```bash
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9sMcM6YcfAFNLRnAHn   # output file from cron
```

## What I Learned
- Cron jobs are scheduled tasks stored in `/etc/cron.d/`
- Scripts run by cron often write output to `/tmp`
- Reading cron scripts reveals what files they create
