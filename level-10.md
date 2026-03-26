# Level 10 → 11

## Concept
Decoding Base64 encoded data.

## Solution
```bash
base64 -d data.txt
# or
cat data.txt | base64 -d
```

## What I Learned
- `base64` encodes binary data as text
- `base64 -d` decodes it back
- Common encoding — NOT encryption
