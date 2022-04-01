Notes for Sensu | Monitoring Kubernetes + Docker, Part 2: Prometheus

## Source:
Author: sensu.io
Category: articles
Updated: 02/02/2021 10:40 AM
Highlights URL: https://readwise.io/bookreview/7493113
SourceUrl: https://sensu.io/blog/monitoring-kubernetes-docker-part-2-prometheus


#### Extras:
**kubernetes** **prometheus** **cncf**




 
-----
 ## Highlights:

### The Prometheus collection is also unauthenticated and unencr...
>The Prometheus collection is also unauthenticated and unencrypted. So, if anything has access to the network, it can observe your telemetry data (this includes metric labels — you add labels for context, but then that context would be out in the open). ^rw140170685hl


Highlighted: 02/01/2021 09:35 PM
Updated: 02/02/2021 07:45 AM


#### Extras:





------

### For ephemeral infrastructure, Prometheus uses a set of disco...
>For ephemeral infrastructure, Prometheus uses a set of discovery libraries to stay up to date with the platforms it monitors (such as Kubernetes). This method introduces a degree of lag as resources come and go, which in turn is exaggerated by metric scraping intervals. ^rw140170683hl


Highlighted: 02/01/2021 09:35 PM
Updated: 02/01/2021 09:35 PM


#### Extras:





------

### While great for Kubernetes, Prometheus is not designed for m...
>While great for Kubernetes, Prometheus is not designed for monitoring legacy or multi-generational infrastructure. One reason for this is because it’s a pull-based system, requiring you to punch holes in the firewalls in traditional networks. ^rw140170670hl


Highlighted: 02/01/2021 09:34 PM
Updated: 02/02/2021 07:37 AM


#### Extras:





------

### get limited granularity with the pulled-based model, because...
>get limited granularity with the pulled-based model, because the exporters provide summarized data, which is only scraped periodically ^rw140170660hl

Comment: and thats the big downside! ^rw140170660comment

Highlighted: 02/01/2021 09:34 PM
Updated: 02/02/2021 07:25 AM


#### Extras:





------

### As with any pure-telemetry monitoring solution, you miss out...
>As with any pure-telemetry monitoring solution, you miss out on context with the simplified, constrained data model. Because all data must be represented as a measurement, it affects how you represent certain pieces of data ^rw140170451hl


Highlighted: 02/01/2021 09:34 PM
Updated: 02/01/2021 09:34 PM


#### Extras:





------

### Prometheus components include
>Prometheus components include ^rw140169214hl

Comment: - main prometheus server
  - retrieval/collection component
- time series db
- api
- alert manager
- pushgateway ^rw140169214comment

Highlighted: 02/01/2021 09:30 PM
Updated: 02/01/2021 09:31 PM


#### Extras:





------

### One of the most unique attributes about Prometheus is that i...
>One of the most unique attributes about Prometheus is that it uses a pull-based architecture ^rw140167816hl

Comment: This is often listed as a strength, showing how hard it is to deal with intake of metrics at a decent scale. But the cost is you lose metrics. ^rw140167816comment

Highlighted: 02/01/2021 09:26 PM
Updated: 02/02/2021 10:40 AM


#### Extras:





------

### Prometheus is an open source monitoring tool originally buil...
>Prometheus is an open source monitoring tool originally built at SoundCloud. Now a standalone open source project, Prometheus followed in Kubernetes’ footsteps to join the Cloud Native Computing Foundation (CNCF) in 2016. ^rw140167324hl


Highlighted: 02/01/2021 09:23 PM
Updated: 02/01/2021 09:23 PM


#### Extras:





------

