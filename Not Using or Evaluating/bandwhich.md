No longer using since as of 02/18/2022 it doesn't work on M1

Source: https://github.com/imsnif/bandwhich


cli tool to display #network util by #process, connection, and remote IP/hostname

![image](https://github.com/imsnif/bandwhich/blob/main/demo.gif?raw=true)

```
USAGE:
    bandwhich [FLAGS] [OPTIONS]

FLAGS:
    -a, --addresses            Show remote addresses table only
    -c, --connections          Show connections table only
    -h, --help                 Prints help information
    -n, --no-resolve           Do not attempt to resolve IPs to their hostnames
    -p, --processes            Show processes table only
    -r, --raw                  Machine friendlier output
    -s, --show-dns             Show DNS queries
    -t, --total-utilization    Show total (cumulative) usages
    -V, --version              Prints version information

OPTIONS:
    -d, --dns-server <dns-server>    A dns server ip to use instead of the system default
    -i, --interface <interface>      The network interface to listen on, eg. eth0
```

