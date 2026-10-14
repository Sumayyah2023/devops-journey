# Day 2 - Linux Fundamentals

## Permissions
- r=4 w=2 x=1 -> 755 scripts, 644 files, 600 secrets, 750 team scripts
- chmod, chown, groupadd, useradd -G

## Processes
- ps aux, pgrep -a, top, kill (SIGTERM) vs kill -9 (SIGKILL, last resort)
- ss -tulnp to see listening ports

## Services
- systemctl start/stop/restart = now; enable/disable = at boot
- journalctl -u <service> for logs

## Log analysis
- Pattern: filter | awk '{print $N}' | sort | uniq -c | sort -rn
- awk '$9 == 404 {print $7}' = 404s by URL
- Found unexpected /wpad.dat hits = Windows WPAD proxy discovery via WSL2 localhost
