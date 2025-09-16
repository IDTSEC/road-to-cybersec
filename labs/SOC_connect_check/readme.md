# SOC connectivity check (demo)

## what it does
- attempts TCP connect to port 80 and 443
- performs HTTPS HEAD request
- prints JSON summary w/ timestamp, latencies, errors

## what i used
```bash
python3 monitor.py example.com
