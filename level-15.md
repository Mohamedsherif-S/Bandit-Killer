# Level 15 → 16

## Concept
Connecting to an SSL/TLS encrypted port.

## Solution
```bash
echo "PASSWORD" | openssl s_client -connect localhost:30001 -quiet
```

## What I Learned
- Regular `nc` can't handle SSL — use `openssl s_client`
- `-quiet` suppresses certificate info
- SSL encrypts the connection between client and server
