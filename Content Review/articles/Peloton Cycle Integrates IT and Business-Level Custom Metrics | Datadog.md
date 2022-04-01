Notes for Peloton Cycle Integrates IT and Business-Level Custom Metrics | Datadog

## Source:
Author: K.Z. Win
Category: articles
Updated: 09/23/2021 05:05 PM
Highlights URL: https://readwise.io/bookreview/11083730
SourceUrl: https://www.datadoghq.com/blog/peloton-cycle-integrates-it-business-custom-metrics/


#### Extras:


 
-----
 ## Highlights:

### This tablet not only serves as a 1080p video screen for cons...
>This tablet not only serves as a 1080p video screen for consuming live coaching sessions from our flagship studio in NYC but it also sends the rider’s performance data via http protocol to one of our many application servers which are running behind the reverse-proxied NGINX. ^rw230404475hl


Highlighted: 09/23/2021 02:18 PM
Updated: 09/23/2021 02:18 PM


#### Extras:



------

### We can get an estimate of the number of live rides by using ...
>We can get an estimate of the number of live rides by using a linear transformation of NGINX requests&#x2F;s
&gt;live rides = (nginx requests&#x2F;s – background requests&#x2F;s)&#x2F;3.1 ^rw230404494hl


Highlighted: 09/23/2021 02:18 PM
Updated: 09/23/2021 02:18 PM


#### Extras:



------

### 3.1 is the typical rate that a rider is sending requests to ...
>3.1 is the typical rate that a rider is sending requests to NGINX ^rw230404521hl


Highlighted: 09/23/2021 02:18 PM
Updated: 09/23/2021 02:18 PM


#### Extras:



------

### For instance, if we get a lot of traffic on our website, htt...
>For instance, if we get a lot of traffic on our website, http requests to other app servers effects the ride count. In addition, an atypical usage pattern during the ride can cause the denominator to deviate somewhat from 3.1. ^rw230404527hl


Highlighted: 09/23/2021 02:19 PM
Updated: 09/23/2021 02:19 PM


#### Extras:



------

### We set up alerts so our log parser reports slow endpoints in...
>We set up alerts so our log parser reports slow endpoints in our Datadog Events Stream as seen below. ^rw230437251hl


Highlighted: 09/23/2021 05:05 PM
Updated: 09/23/2021 05:05 PM


#### Extras:





------

### With a little additional effort, we rewrote our log parser t...
>With a little additional effort, we rewrote our log parser to send all NGINX requests data to a local DogStatsD server. This UDP server comes with any machine running the Datadog agent and takes care of periodically flushing accumulated data to the metric server. Essentially we now use web counters as described in the Sending Metrics with DogStatsD guide and tag each hit with a normalized URL. Now that this counter metric is set up we can treat the data as equivalent to NGINX request&#x2F;s and we can more accurately count the number of rides by keeping track of requests&#x2F;s for one specific endpoint. If no rides are happening this metric is appropriately missing instead of reporting 0.1 or 0.3 as in our previous case. The time series graph below shows the number of live rides over a 24-hours period. ^rw230404615hl


Highlighted: 09/23/2021 02:20 PM
Updated: 09/23/2021 02:20 PM


#### Extras:



------

