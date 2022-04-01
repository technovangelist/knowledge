Notes for Microservice Observability — Metrics | by Siben Nayak | Medium

## Source:
Author: Siben Nayak
Category: articles
Updated: 09/23/2021 06:32 PM
Highlights URL: https://readwise.io/bookreview/11086960
SourceUrl: https://betterprogramming.pub/microservice-observability-metrics-bd9be270bc62


#### Extras:




 
-----
 ## Highlights:

### Golden signals
Golden signals are an effective way of monito...
>Golden signals
Golden signals are an effective way of monitoring the overall state of the system and identifying problems. ^rw230455012hl

Comment: - Availability: State of your system measured from the perspective of clients (e.g. percentage of errors on total requests).
- Health: State of your system measured using periodic pings.
- Request rate: Rate of incoming requests to the system.
- Saturation: How free or loaded the system is (e.g. queue depth or available memory).
- Utilization: How busy the system is (e.g. CPU load or memory usage). This is represented in percentage.
- Error rate: Rate of errors being produced in the system.
- Latency: Response time of the system, usually measured in the 95th or 99th percentile. ^rw230455012comment

Highlighted: 09/23/2021 06:28 PM
Updated: 09/23/2021 06:29 PM


#### Extras:





------

### Availability: State of your system measured from the perspec...
>Availability: State of your system measured from the perspective of clients (e.g. percentage of errors on total requests).
Health: State of your system measured using periodic pings.
Request rate: Rate of incoming requests to the system.
Saturation: How free or loaded the system is (e.g. queue depth or available memory).
Utilization: How busy the system is (e.g. CPU load or memory usage). This is represented in percentage.
Error rate: Rate of errors being produced in the system.
Latency: Response time of the system, usually measured in the 95th or 99th percentile. ^rw230455024hl


Highlighted: 09/23/2021 06:28 PM
Updated: 09/23/2021 06:28 PM


#### Extras:





------

### Memex note from: 2021-9-23 18:29:35
>Memex note from: 2021-9-23 18:29:35 ^rw230455065hl

Comment: - Availability: State of your system measured from the perspective of clients (e.g. percentage of errors on total requests).
- Health: State of your system measured using periodic pings.
- Request rate: Rate of incoming requests to the system.
- Saturation: How free or loaded the system is (e.g. queue depth or available memory).
- Utilization: How busy the system is (e.g. CPU load or memory usage). This is represented in percentage.
- Error rate: Rate of errors being produced in the system.
- Latency: Response time of the system, usually measured in the 95th or 99th percentile. ^rw230455065comment

Highlighted: 09/23/2021 06:29 PM
Updated: 09/23/2021 06:29 PM


#### Extras:





------

### Memex note from: 2021-9-23 18:29:59
>Memex note from: 2021-9-23 18:29:59 ^rw230455131hl


Highlighted: 09/23/2021 06:29 PM
Updated: 09/23/2021 06:29 PM


#### Extras:





------

### Resource metrics are almost always made available by default...
>Resource metrics are almost always made available by default from the infrastructure provider (AWS CloudWatch or Kubernetes metrics) and are used to monitor infrastructure health. ^rw230455157hl

Comment: - CPU&#x2F;memory utilization: Usage of the system’s core resources.
- Host count: Number of hosts&#x2F;pods that are running your system (used to detect availability issues due to pod crashes).
- Live threads: Threads spawned in your service (used to detect issues in multi-threading).
- Heap usage: Heap memory usage statistics (can help debug memory leaks). ^rw230455157comment

Highlighted: 09/23/2021 06:30 PM
Updated: 09/23/2021 06:30 PM


#### Extras:





------

### Business metrics can be used to monitor granular interaction...
>Business metrics can be used to monitor granular interaction with core APIs or functionality in your services ^rw230455366hl

Comment: disappointing that they think these are business metrics ^rw230455366comment

Highlighted: 09/23/2021 06:31 PM
Updated: 09/23/2021 06:32 PM


#### Extras:





------

