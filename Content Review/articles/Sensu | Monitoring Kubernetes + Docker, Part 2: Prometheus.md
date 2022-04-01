Notes for Sensu | Monitoring Kubernetes + Docker, Part 2: Prometheus

## Source:
Author: sensu.io
Category: articles
Updated: 02/02/2021 10:40 AM
Highlights URL: https://readwise.io/bookreview/7493113
SourceUrl: https://sensu.io/blog/monitoring-kubernetes-docker-part-2-prometheus

%%7493113topstart%%
#### Extras:
[[kubernetes]] [[prometheus]] [[cncf]]

%%7493113topend%%


 
-----
 ## Highlights:

### The Prometheus collection is also unauthenticated and unencr...
>The Prometheus collection is also unauthenticated and unencrypted. So, if anything has access to the network, it can observe your telemetry data (this includes metric labels — you add labels for context, but then that context would be out in the open). ^rw140170685hl


Highlighted: 02/01/2021 09:35 PM
Updated: 02/02/2021 07:45 AM

%%140170685start%%
#### Extras:

%%140170685end%%



------

### For ephemeral infrastructure, Prometheus uses a set of disco...
>For ephemeral infrastructure, Prometheus uses a set of discovery libraries to stay up to date with the platforms it monitors (such as Kubernetes). This method introduces a degree of lag as resources come and go, which in turn is exaggerated by metric scraping intervals. ^rw140170683hl


Highlighted: 02/01/2021 09:35 PM
Updated: 02/01/2021 09:35 PM

%%140170683start%%
#### Extras:

%%140170683end%%



------

### While great for Kubernetes, Prometheus is not designed for m...
>While great for Kubernetes, Prometheus is not designed for monitoring legacy or multi-generational infrastructure. One reason for this is because it’s a pull-based system, requiring you to punch holes in the firewalls in traditional networks. ^rw140170670hl


Highlighted: 02/01/2021 09:34 PM
Updated: 02/02/2021 07:37 AM

%%140170670start%%
#### Extras:

%%140170670end%%



------

### get limited granularity with the pulled-based model, because...
>get limited granularity with the pulled-based model, because the exporters provide summarized data, which is only scraped periodically ^rw140170660hl

Comment: and thats the big downside! ^rw140170660comment

Highlighted: 02/01/2021 09:34 PM
Updated: 02/02/2021 07:25 AM

%%140170660start%%
#### Extras:

%%140170660end%%



------

### As with any pure-telemetry monitoring solution, you miss out...
>As with any pure-telemetry monitoring solution, you miss out on context with the simplified, constrained data model. Because all data must be represented as a measurement, it affects how you represent certain pieces of data ^rw140170451hl


Highlighted: 02/01/2021 09:34 PM
Updated: 02/01/2021 09:34 PM

%%140170451start%%
#### Extras:

%%140170451end%%



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

%%140169214start%%
#### Extras:

%%140169214end%%



------

### One of the most unique attributes about Prometheus is that i...
>One of the most unique attributes about Prometheus is that it uses a pull-based architecture ^rw140167816hl

Comment: This is often listed as a strength, showing how hard it is to deal with intake of metrics at a decent scale. But the cost is you lose metrics. ^rw140167816comment

Highlighted: 02/01/2021 09:26 PM
Updated: 02/02/2021 10:40 AM

%%140167816start%%
#### Extras:

%%140167816end%%



------

### Prometheus is an open source monitoring tool originally buil...
>Prometheus is an open source monitoring tool originally built at SoundCloud. Now a standalone open source project, Prometheus followed in Kubernetes’ footsteps to join the Cloud Native Computing Foundation (CNCF) in 2016. ^rw140167324hl


Highlighted: 02/01/2021 09:23 PM
Updated: 02/01/2021 09:23 PM

%%140167324start%%
#### Extras:

%%140167324end%%



------

