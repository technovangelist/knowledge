Notes for Building Highly Reliable Data Pipelines at Datadog | Datadog

## Source:
Author: Quentin Francois
Category: articles
Updated: 02/03/2021 10:07 AM
Highlights URL: https://readwise.io/bookreview/7521294
SourceUrl: https://www.datadoghq.com/blog/engineering/highly-reliable-data-pipelines/


#### Extras:
**datadog** **monitoring** **spark**



 
-----
 ## Highlights:

### Think about failures ahead of time and get prepared to recov...
>Think about failures ahead of time and get prepared to recover fast from failures. ^rw140911654hl


Highlighted: 02/03/2021 10:07 AM
Updated: 02/03/2021 10:07 AM


#### Extras:





------

### Monitor cluster metrics, job metrics, and data latencies met...
>Monitor cluster metrics, job metrics, and data latencies metrics to detect failures early. ^rw140911652hl


Highlighted: 02/03/2021 10:07 AM
Updated: 02/03/2021 10:07 AM


#### Extras:





------

### Break down jobs into small, survivable pieces to reduce lost...
>Break down jobs into small, survivable pieces to reduce lost work in the event of failures ^rw140911651hl


Highlighted: 02/03/2021 10:07 AM
Updated: 02/03/2021 10:07 AM


#### Extras:





------

### Remember that reliability is a matter of time constraints: y...
>Remember that reliability is a matter of time constraints: you need to agree on the latency requirements with the downstream users of your data pipelines. The latency requirements will determine how much effort you’ll have to spend to make your pipeline highly reliable ^rw140911649hl


Highlighted: 02/03/2021 10:06 AM
Updated: 02/03/2021 10:06 AM


#### Extras:





------

### Meanwhile, memory usage is a tricky thing to manage in Spark...
>Meanwhile, memory usage is a tricky thing to manage in Spark, and lots of failures are due to a shortage of memory. The Agent can report memory metrics by executor in the Heat Map. The graph above shows the maximum memory usage by executor. Some executors are reaching the limits and then suddenly dropping, because they’re running out of memory ^rw140911420hl

Comment: ![](https://imgix.datadoghq.com/img/blog/engineering/highly-reliable-data-pipelines/hrdp-cluster_metrics2.png?auto=format&fit=max&w=847&dpr=2) ^rw140911420comment

Highlighted: 02/03/2021 10:05 AM
Updated: 02/03/2021 10:05 AM


#### Extras:





------

### This graph shows the percentage of disk used by a node on a ...
>This graph shows the percentage of disk used by a node on a given cluster. The first three jobs are running fine, they have plenty of room—but the last job is eating up a lot more disk, and some nodes have run out of disk space. So we can tell that this job has failed. We set up alerts for when our jobs are running out of disk, which means that we may need to add more nodes to the cluster. ^rw140908280hl

Comment: ![](https://imgix.datadoghq.com/img/blog/engineering/highly-reliable-data-pipelines/hrdp-cluster_metrics.png?auto=format&fit=max&w=847&dpr=2) ^rw140908280comment

Highlighted: 02/03/2021 10:02 AM
Updated: 02/03/2021 10:02 AM


#### Extras:





------

### We do this by tagging our clusters
>We do this by tagging our clusters ^rw140901322hl

Comment: We tag our clusters so that we can see metrics cluster by cluster. 
![](https://imgix.datadoghq.com/img/blog/engineering/highly-reliable-data-pipelines/hrdp-cluster-filtering.png?auto=format&fit=max&w=847&dpr=2) ^rw140901322comment

Highlighted: 02/03/2021 09:32 AM
Updated: 02/03/2021 10:03 AM


#### Extras:





------

### 14 hours
>14 hours ^rw140900108hl

Comment: The time it takes to run the rollup job. By splitting it up into lots of smaller jobs can deal with spot instances ^rw140900108comment

Highlighted: 02/03/2021 09:30 AM
Updated: 02/03/2021 09:31 AM


#### Extras:





------

### Broadly: don’t have long running jobs. The longer the job, t...
>Broadly: don’t have long running jobs. The longer the job, the more work you lose when you have a cluster problem, and the longer it takes to recover from a failed job. ^rw140899459hl

Comment: If you have clusters that disappear at any time, such as when hosted on AWS Spot Instances, solve it by keeping everything short. ^rw140899459comment

Highlighted: 02/03/2021 09:29 AM
Updated: 02/03/2021 09:29 AM


#### Extras:





------

### In order to ensure on-demand resources for their users, Amaz...
>In order to ensure on-demand resources for their users, Amazon needs to have a lot of excess servers. Most of the time, these excess servers are unused, so they make them available at discounts on the spot market. You can get ridiculous savings using spot instances, up to 80% off the on-demand price—but the downside is your clusters can disappear at any time depending on supply and demand. It’s like having chaos monkeys randomly killing nodes in your clusters ^rw140899331hl


Highlighted: 02/03/2021 09:28 AM
Updated: 02/03/2021 09:28 AM


#### Extras:





------

### “Reliability is the probability that a system will produce c...
>“Reliability is the probability that a system will produce correct outputs up to some given time
>Source: E.J. McClusky & S. Mitra (2004). "Fault Tolerance" in Computer Science Handbook 2ed. ed. A.B. Tucker. CRC Press ^rw140876878hl


Highlighted: 02/03/2021 08:21 AM
Updated: 02/03/2021 08:21 AM


#### Extras:





------

