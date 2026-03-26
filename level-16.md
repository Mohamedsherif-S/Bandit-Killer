# Level 16 → 17

## Concept
Finding open ports in a range using Nmap, then connecting with SSL.

## Solution
```bash
nmap -p 31000:32000 localhost      # scan port range
openssl s_client -connect localhost:31790 -quiet
# submit password → receive private SSH key
```

## What I Learned
- `nmap -p start:end host` scans a port range
- Some ports speak SSL, some don't — test each
- Server can respond with an SSH private key
