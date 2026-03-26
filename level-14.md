# Level 14 → 15

## Concept
Sending data to a port using Netcat.

## Solution
```bash
echo "PASSWORD" | nc localhost 30000
```

## What I Learned
- `nc hostname port` opens a TCP connection
- Piping with `echo` sends data to the port
- Netcat is the "Swiss army knife" of networking
