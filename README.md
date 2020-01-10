# Tips & Tricks for everyday usage

# Bash

## SOCKS5 proxy with ssh client

Makes any ssh server your personal SOCKS5 proxy. Automatically reconnects after connection timeout. Just run command below and use 127.0.0.1:1080 as a proxy address anywhere you need it.

```bash
$(exit 1) || while [ $? -ne 0 ]; do ssh  -o ServerAliveInterval=5 -D 1080 -N  user@example.com;done
```
