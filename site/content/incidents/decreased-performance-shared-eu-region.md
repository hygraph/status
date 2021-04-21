+++
title = "Decreased Performance Shared EU region"
date = 2021-04-20T15:35:23.000Z
severity = "degraded-performance"
affectedsystems = [
  "Content API"
]
resolved = true
+++
Our team is currently investigating an increasing error rate on the Shared EU Region

**Update**: Our engineers are continuing to work on resolving the current API errors on the shared EU region {{< track "2021-04-20T15:48:23.000Z" >}}

**Update**: We are continuing to investigate this issue.  {{< track "2021-04-20T16:25:00.000Z" >}}

**Update**: We are continuing to investigate this issue.  {{< track "2021-04-20T17:25:00.000Z" >}}

**Update**: We are continuing to investigate this issue. We know it's a real inconvenience and hope to have it resolved soon  {{< track "2021-04-20T18:00:00.000Z" >}}

**Update**: The API error rate is decreasing and the APIs should be available again. Our team is continuing to monitor. {{< track "2021-04-20T18:20:00.000Z" >}}

**Resolved**: The service in our shared EU region is fully recovered now. {{< track "2021-04-20T18:20:00.000Z" >}}

## Post Mortem
The Central Europe content DB became unavailable from 17:45 to 20:20 CEST on April 20th 2021. During that time we observed increased error rate in that region's Content API and the global Management API. Also, schema migrations stopped executing. 

This incident was caused by a high load on the Content API in the shared EU region which lead to  memory pressure on the underlaying database. As a result the error rate increased and API requests began failing.

Our infrastructure team tried upscaling the database to make sure it could handle the increased load. This modification took longer than anticipated and did not work with the regular failover mechanism, thus causing a downtime for the API. 

To make sure this won't happen again we have put more detailed metrics in place to ensure that database modifications will only be applied when certain criterias are met. Also the db connection handling that is used for schema migrations was improved to guarantee better isolation across regions in such scenarios.