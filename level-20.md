# Level 20 → 21

## Concept
Using Netcat as a server and a SUID binary that connects back.

## Solution
```bash
# Terminal 1 — set up listener with current password
echo "PASSWORD" | nc -l -p 1234 &

# Terminal 2 — run the SUID binary
./suconnect 1234
```

## What I Learned
- `nc -l -p PORT` listens as a server
- `&` runs a process in the background
- The binary connects to our listener, verifies the password, sends next one
