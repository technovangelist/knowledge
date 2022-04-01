Notes for End-To-End Application Monitoring With Datadog | Datadog

## Source:
Author: datadoghq.com
Category: articles
Updated: 02/03/2021 04:04 PM
Highlights URL: https://readwise.io/bookreview/7526915
SourceUrl: https://www.datadoghq.com/blog/end-to-end-application-monitoring/


#### Extras:




 
-----
 ## Highlights:

### A dotted vertical line on each timeseries graph indicates th...
>A dotted vertical line on each timeseries graph indicates the time of the trace, making it easy for you to correlate the request with the metrics displayed. For example, in the screenshot below, the RSS Memory graph shows that the container’s memory consumption had been rising steadily leading up to the trace that threw a 500 error. This information can help you focus your investigation on how the service uses memory, knowing that there was not a corresponding spike in CPU usage at the time of the trace. ^rw141015378hl

Comment: ![](https://imgix.datadoghq.com/img/blog/end-to-end-application-monitoring/end-to-end-application-monitoring-metrics-container.png?auto=format&fit=max&w=847&dpr=2) ^rw141015378comment

Highlighted: 02/03/2021 04:04 PM
Updated: 02/03/2021 04:04 PM


#### Extras:





------

### In the screenshot below, we’ve clicked on the session.id tag...
>In the screenshot below, we’ve clicked on the session.id tag to pivot to the RUM Explorer, where we can reconstruct the user session. This can be helpful, for example, in determining whether a bug is associated with a particular user, browser, location, or other condition ^rw141015282hl

Comment: ![](https://imgix.datadoghq.com/img/blog/end-to-end-application-monitoring/end-to-end-application-monitoring-rum.png?auto=format&fit=max&w=847&dpr=2) ^rw141015282comment

Highlighted: 02/03/2021 04:03 PM
Updated: 02/03/2021 04:03 PM


#### Extras:
**rum**




------

### For example, you can use the env tag to view all the request...
>For example, you can use the env tag to view all the requests within a single environment or the http.base_url tag to see all the requests to a single endpoint ^rw141015221hl

Comment: neat uses of tags ^rw141015221comment

Highlighted: 02/03/2021 04:02 PM
Updated: 02/03/2021 04:02 PM


#### Extras:





------

