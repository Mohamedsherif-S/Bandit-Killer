# Level 12 → 13

## Concept
Decompressing a file that has been compressed multiple times.

## Solution
```bash
mkdir /tmp/work && cp data.txt /tmp/work && cd /tmp/work
xxd -r data.txt > data.bin    # reverse hexdump
file data.bin                  # check type, then decompress accordingly

# Repeat with appropriate tool:
gzip -d file.gz
bzip2 -d file.bz2
tar -xf file.tar
```

## What I Learned
- `xxd -r` reverses a hex dump back to binary
- `file` identifies compression type
- Multiple compression layers require repeated decompression
- Tools: `gzip`, `bzip2`, `tar`
