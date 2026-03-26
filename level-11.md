# Level 11 → 12

## Concept
Decoding ROT13 cipher.

## Solution
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

## What I Learned
- ROT13 shifts each letter by 13 positions
- `tr` translates characters — maps A-M to N-Z and vice versa
- ROT13 is its own inverse (apply twice = original)
