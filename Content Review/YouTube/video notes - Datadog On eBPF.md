Notes for Datadog On eBPF

## Source:
Author: Datadog
Title: Datadog On eBPF
Category: YouTube
Published: 02/03/2021 06:37 AM
 ^yt58KtGtpn0gabout
%%58KtGtpn0_gtopstart%%
#### Extras:
[ebpf](/knowledge/Other Notes/ebpf.md) **datadognpm**
%%58KtGtpn0_gtopend%%

-----
## Highlights:

Timecode: [4:04](https://www.youtube.com/watch?v=58KtGtpn0_g&t=244) ^yt58KtGtpn0g244t

Comment: 
>eBPF is a set of technologies that can run sandboxed programs in the Linux kernel without changing kernel source code or having to load kernel modules ^yt58KtGtpn0g244c
%%244start%%
#### Extras:

What is the set of technologies that can run sandboxed programs in the Linux kernel without changing kernel source code or having to load kernel modules? #flashcard 
eBPF, or Extended Berkeley Packet Filter
<!--ID: 1612593905288-->


%%244end%%


-----
Timecode: [4:47](https://www.youtube.com/watch?v=58KtGtpn0_g&t=287) ^yt58KtGtpn0g287t

Comment: 
>bpf added in 1992. was a bytecode in-kernal interpreter. allowed to define fcn to take packet to boolean. used in tcpdump. ^yt58KtGtpn0g287c
%%287start%%
#### Extras:

When was bpf (not ebpf) added to the Linux kernel? #flashcard 
1992
<!--ID: 1612593905301-->


%%287end%%


-----
Timecode: [5:15](https://www.youtube.com/watch?v=58KtGtpn0_g&t=315) ^yt58KtGtpn0g315t

Comment: 
>ebpf started in 2014 ^yt58KtGtpn0g315c
%%315start%%
#### Extras:

%%315end%%


-----
Timecode: [5:55](https://www.youtube.com/watch?v=58KtGtpn0_g&t=355) ^yt58KtGtpn0g355t

Comment: 
>![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/6quQLEw9/488c500b-fa8a-44c7-963f-ff92c1a4a022.jpg?v=13c4910a58d38ffdb934bb70742eb69c) ^yt58KtGtpn0g355c
%%355start%%
#### Extras:

%%355end%%


-----
Timecode: [6:08](https://www.youtube.com/watch?v=58KtGtpn0_g&t=368) ^yt58KtGtpn0g368t

Comment: 
>kprobes added in 4.1 - used to attached to any function in the kernel. so anything in the kernel source code, you can instrument ^yt58KtGtpn0g368c
%%368start%%
#### Extras:

%%368end%%


-----
Timecode: [6:15](https://www.youtube.com/watch?v=58KtGtpn0_g&t=375) ^yt58KtGtpn0g375t

Comment: 
>In 4.4 added perf buffers. data structure that allows ebpf programs to be written in more event driven manner ^yt58KtGtpn0g375c
%%375start%%
#### Extras:

%%375end%%


-----
Timecode: [6:28](https://www.youtube.com/watch?v=58KtGtpn0_g&t=388) ^yt58KtGtpn0g388t

Comment: 
>4.7 added tracepoints support - abi stable version of kprobes. what is abi stable? Got clarification from Lee. ABI stability is relatively common if you work in a language where static linking is a thing (like C, C++, and rust). there are a bunch of articles on it wrt swift such as [ABI Stability Manifesto in the Swift repo](https://github.com/apple/swift/blob/main/docs/ABIStabilityManifesto.md) ^yt58KtGtpn0g388c
%%388start%%
#### Extras:

%%388end%%


-----
Timecode: [6:38](https://www.youtube.com/watch?v=58KtGtpn0_g&t=398) ^yt58KtGtpn0g398t

Comment: 
>4.8 added XDP - express data path. allows ebpf programs to operate just before packet entered or left machine. unlocked the ability for tools like cilium ^yt58KtGtpn0g398c
%%398start%%
#### Extras:

%%398end%%


-----
Timecode: [6:52](https://www.youtube.com/watch?v=58KtGtpn0_g&t=412) ^yt58KtGtpn0g412t

Comment: 
>cilium is a k8s cni that datadog uses quite a bit ^yt58KtGtpn0g412c
%%412start%%
#### Extras:

%%412end%%


-----
Timecode: [7:02](https://www.youtube.com/watch?v=58KtGtpn0_g&t=422) ^yt58KtGtpn0g422t

Comment: 
>4.10 added cgroups - allows you to add network security policies to containers ^yt58KtGtpn0g422c
%%422start%%
#### Extras:

%%422end%%


-----
Timecode: [7:21](https://www.youtube.com/watch?v=58KtGtpn0_g&t=441) ^yt58KtGtpn0g441t

Comment: 
>since then so much added with every release ^yt58KtGtpn0g441c
%%441start%%
#### Extras:

%%441end%%


-----
Timecode: [8:07](https://www.youtube.com/watch?v=58KtGtpn0_g&t=487) ^yt58KtGtpn0g487t

Comment: 
>most important reason for the hype of ebpf: stability ^yt58KtGtpn0g487c
%%487start%%
#### Extras:

%%487end%%


-----
Timecode: [8:41](https://www.youtube.com/watch?v=58KtGtpn0_g&t=521) ^yt58KtGtpn0g521t

Comment: 
>before ebpf, tools that did that kind of functionality would require updates to the kernel and updates to the OS might interupt the ability to use the tool. Now tool vendors can supply great functionality without the need to update the OS and therefore not lock you to a specific version of the OS ^yt58KtGtpn0g521c
%%521start%%
#### Extras:

%%521end%%


-----
Timecode: [9:09](https://www.youtube.com/watch?v=58KtGtpn0_g&t=549) ^yt58KtGtpn0g549t

Comment: 
>the alternatives including
>1. relying on userspace instrumentation which can be super patchy
>2. rely on older kernel apis which may not expose all that you need
>3. write your own kernel driver which is very dangerous. can crash the system ^yt58KtGtpn0g549c
%%549start%%
#### Extras:

%%549end%%


-----
Timecode: [10:16](https://www.youtube.com/watch?v=58KtGtpn0_g&t=616) ^yt58KtGtpn0g616t

Comment: 
>![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/rRukLOkb/8ca03770-2ee6-455e-8de4-d0bd67f871ae.jpg?v=6cb95913653b214a1e2bd9c0a7ad3a86) ^yt58KtGtpn0g616c
%%616start%%
#### Extras:

%%616end%%


-----
Timecode: [16:47](https://www.youtube.com/watch?v=58KtGtpn0_g&t=1007) ^yt58KtGtpn0g1007t

Comment: 
>https://github.com/DataDog/ebpf ^yt58KtGtpn0g1007c
%%1007start%%
#### Extras:

%%1007end%%


-----
Timecode: [20:46](https://www.youtube.com/watch?v=58KtGtpn0_g&t=1246) ^yt58KtGtpn0g1246t

Comment: 
>one of the hard things with getting started with ebpf is seeing examples of how to do stuff. the repo shared is public and open source and includes lots of examples ^yt58KtGtpn0g1246c
%%1246start%%
#### Extras:

%%1246end%%


-----
Timecode: [27:10](https://www.youtube.com/watch?v=58KtGtpn0_g&t=1630) ^yt58KtGtpn0g1630t

Comment: 
>network monitoring feature of datadog doesn't capture packets, just the metadata ^yt58KtGtpn0g1630c
%%1630start%%
#### Extras:

%%1630end%%


-----
Timecode: [27:39](https://www.youtube.com/watch?v=58KtGtpn0_g&t=1659) ^yt58KtGtpn0g1659t

Comment: 
>walks through how to interpret the following graph
>https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/d5uwenvR/47e095d7-4c40-4e8e-9680-8b9190752f2a.jpg?v=80a0a90f907ffc9b160643583807d6ae) ^yt58KtGtpn0g1659c
%%1659start%%
#### Extras:
hmm, the image didn't come through: ![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/d5uwenvR/47e095d7-4c40-4e8e-9680-8b9190752f2a.jpg?v=80a0a90f907ffc9b160643583807d6ae
%%1659end%%


-----
Timecode: [28:26](https://www.youtube.com/watch?v=58KtGtpn0_g&t=1706) ^yt58KtGtpn0g1706t

Comment: 
>network topology view ^yt58KtGtpn0g1706c
%%1706start%%
#### Extras:
![](https://p-qkfgo2.t2.n0.cdn.getcloudapp.com/items/nOulmblo/8911ec6a-02b5-4970-a6d6-6276e682e8db.jpg?v=4801a0120412ea640627cb0a911be704)
%%1706end%%


-----
Timecode: [33:19](https://www.youtube.com/watch?v=58KtGtpn0_g&t=1999) ^yt58KtGtpn0g1999t

Comment: 
>esr = event security review ^yt58KtGtpn0g1999c
%%1999start%%
#### Extras:

%%1999end%%


-----
Timecode: [34:05](https://www.youtube.com/watch?v=58KtGtpn0_g&t=2045) ^yt58KtGtpn0g2045t

Comment: 
>how we do process execution monitoring ^yt58KtGtpn0g2045c
%%2045start%%
#### Extras:

%%2045end%%


-----
Timecode: [45:23](https://www.youtube.com/watch?v=58KtGtpn0_g&t=2723) ^yt58KtGtpn0g2723t

Comment: 
>is there a limit to the size of the ebpf map? Guillaume answers. ^yt58KtGtpn0g2723c
%%2723start%%
#### Extras:

%%2723end%%



## Video Description on YouTube:
eBPF (extended Berkeley Packet Filter) is a Linux technology that can run sandboxed programs in the kernel without changing kernel source code or loading kernel modules. While the kernel is an ideal place to implement monitoring/observability, networking, and security it wasn't until the recent broad adoption of eBPF that it was feasible.

Datadog has embraced the possibilities that eBPF brings in those areas and there are several teams already using eBPF in their products. 

In this session Ara Pulido, Technical Evangelist, chats with Guillaume Fournier, security engineer on the Security Agent team and Lee Avital, Team Lead on the Networks team. Both teams are using eBPF in production at Datadog. We cover what eBPF is, the problem it solves, and how it is currently being used for network monitoring and security.

By the end of the session you will have a better understanding of what eBPF is, why so many organizations are adopting this new technology, and how eBPF can benefit your organization.