+++
title = "Permission System Maintenance"
date = 2020-11-11T17:00:00.000Z
severity = "under-maintenance"
affectedsystems = [
  "Management API"
]
resolved = false
+++
We are preparing a larger migration to introduce the ground work for upcoming features. For this we have to migrate all existing customer projects so they are able to use the new Permission Engine we already put in place. In the first step you won’t notice any differences, since the new permission system will work exactly the same from the outside. 

For the migration we need to stop write mutations on the management API for a short time, so no schema changes, migrations and project creations will be possible during this time window. 

**The migration will start today at 6pm CET** and will most likely take 2 hours. We will post updates on our status page accordingly.

**Update**: The maintenance has started. {{< track "2020-11-11T17:01:00.000Z" >}}

**Update**: The maintenance is progressing, we are taking the final steps. {{< track "2020-11-11T19:01:00.000Z" >}}

**Update**: The maintenance is nearly completed, our team is monitoring the changes. {{< track "2020-11-11T19:20:00.000Z" >}}