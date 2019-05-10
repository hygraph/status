+++
title = "Schema Changes & API Outage due to AWS Issues"
date = 2019-05-10T08:17:31.000Z
severity = "degraded-performance"
affectedsystems = [
  "WebApp"
]
resolved = true
+++
We are currently facing an issue causing some schema changes in the EU region resulting into a deployment error. Our Engineers are already looking into the issue!

**Update**: Some APIs seems to be affected by the issue, we are working on getting them back up asap. {{< track "2018-05-10T09:38:00.000Z" >}}

**Update**: It seems that our AWS database is affected by a general issue on AWS' side. See here for further information [https://status.aws.amazon.com/](https://status.aws.amazon.com/#EU_block) {{< track "2018-05-10T09:40:00.000Z" >}}

**Update**: Our EU-West region is slowly recovering. We are continuing to monitor this region. {{< track "2018-05-10T10:10:00.000Z" >}}

**Update**: Our EU-West region is slowly recovering. We are continuing to monitor this region. {{< track "2018-05-10T10:10:00.000Z" >}}

**Update**: We are now working on getting the degraded schema changes performance up to speed! {{< track "2018-05-10T10:20:00.000Z" >}}

**Resolved**: Schema Changes are now fully working again on EU. Failed Deployments during that time have been restored manually. {{< track "2018-05-10T14:30:00.000Z" >}}