Notes for Learn eBPF Tracing: Tutorial and Examples

## Source:
Author: brendangregg.com
Category: articles
Updated: 02/04/2021 12:04 PM
Highlights URL: https://readwise.io/bookreview/7348325
SourceUrl: http://www.brendangregg.com/blog/2019-01-01/learn-ebpf-tracing.html


#### Extras:
[ebpf](/knowledge/Other Notes/ebpf)**Brendan Gregg**



 
-----
 ## Highlights:

### What is an example of eBPF tracing?
This eBPF-based tool sho...
>What is an example of eBPF tracing?
This eBPF-based tool shows completed TCP sessions, with their process ID (PID) and command name (COMM), sent and received bytes (TX_KB, RX_KB), and duration in milliseconds (MS
>tcplife
PID   COMM       LADDR           LPORT RADDR           RPORT TX_KB RX_KB MS
22597 recordProg 127.0.0.1       46644 127.0.0.1       28527     0     0 0.23
3277  redis-serv 127.0.0.1       28527 127.0.0.1       46644     0     0 0.28
22598 curl       100.66.3.172    61620 52.205.89.26    80        0     1 91.79
22604 curl       100.66.3.172    44400 52.204.43.121   80        0     1 121.38
22624 recordProg 127.0.0.1       46648 127.0.0.1       28527     0     0 0.22
3277  redis-serv 127.0.0.1       28527 127.0.0.1       46648     0     0 0.27
22647 recordProg 127.0.0.1       46650 127.0.0.1       28527     0     0 0.21
3277  redis-serv 127.0.0.1       28527 127.0.0.1       46650     0     0 0.26
>eBPF did not make this possible – I can rewrite tcplife to use older kernel technologies. But if I did, we'd never run such a tool in production due to the performance overhead, security issues, or both. What eBPF did was make this tool practical: it is efficient and secure. For example, it does not trace every packet like older techniques, which can add too much performance overhead. Instead, it only traces TCP session events, which are much less frequent. This makes the overhead so low we can run this tool in production, 24x7. ^rw136582121hl

Comment: since this is triggered on tcp session events and not every packet, its more efficient, more secure, and has all the info the user actually needs. ^rw136582121comment

Highlighted: 01/26/2021 09:10 AM
Updated: 01/26/2021 09:11 AM


#### Extras:





------

### For tracing, the main ones are bcc and bpftrace.
>For tracing, the main ones are bcc and bpftrace. ^rw136581948hl

Comment: rather than writing a program with direct knowledge of ebpf, you write it using a framework, like bcc or bpftrace. This simplifies things. ^rw136581948comment

Highlighted: 01/26/2021 09:08 AM
Updated: 01/26/2021 09:09 AM


#### Extras:





------

### eBPF does to Linux what JavaScript does to HTML. (Sort of.)
>eBPF does to Linux what JavaScript does to HTML. (Sort of.) ^rw136581339hl

Comment: with ebpf, you can write a program that runs in a vm in the kernel rather than direct in the kernel. this vm has access to all of the networking features, but now your programs don't need to recompile the kernel ^rw136581339comment

Highlighted: 01/26/2021 09:06 AM
Updated: 02/04/2021 12:04 PM


#### Extras:





------

