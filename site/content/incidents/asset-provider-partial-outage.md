+++
title = "Asset provider partial outage"
date = 2021-02-10T20:10:01.000Z
severity = "partial-outage"
affectedsystems = [
  "Asset CDN"
]
resolved = false
+++

Our external service used for Asset handling is currently experiencing issues. Uploading and fetching assets, as well as project creation and deletion might not work as expected. Once we have further information we will be updating the status of this incident.

**Update**: The external team is stil working on resolving the issue. {{< track "2021-02-10T21:00:00.000Z" >}}

**Update**: The outage seems to be related to an issue on AWS Loadbalancers (https://status.aws.amazon.com/). Our Asset provider has provisioned emergency load balancers. Delivery and transformation of assets should be back to normal. Uploads are still affected. {{< track "2021-02-10T21:20:00.000Z" >}}