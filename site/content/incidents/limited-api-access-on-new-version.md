+++
title = "Limited API Access on new Version"
date = 2018-12-12T07:00:38.000Z
severity = "partial-outage"
affectedsystems = [
  "New API"
]
resolved = true
+++
We have identified a cache issue after our migration yesterday and are currently in the process of fixing it. During this time you might see some limited API Access.

**Update**: We have identified the issue that causes a query with a boolean check in the `where`-argument to fail. Our Engineers are working on a fix for this! {{< track "2018-12-12T10:30:00.000Z" >}}

**Resolved**: We just deployed a fix for the boolean where argument error! {{< track "2018-12-12T11:10:00.000Z" >}}
