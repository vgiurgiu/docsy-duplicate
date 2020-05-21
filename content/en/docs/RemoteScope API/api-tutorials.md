---
title: "API tutorials"
date: 2020-03-27
weight: 5
description: >
  API tutorials demonstrate how to use the API methods to satisfy use cases
---

{{% pageinfo %}}
Basic, advanced use cases demonstrated as tutorials.
{{% /pageinfo %}}


## Remote telescope booking

This section describes how to automate remote telescope booking


## Remote telescope operation

For example, point the telescope at one point in the sky for the first half of your observation time, then point it to another part of the sky.

## (NEW!) Remote astrophotography

Starting March 2020, we have equipped a number of telescopes with powerful cameras, so you can now perform astrophotography tasks using RemoteScope.

Simply schedule your observation plan and it will be queued and executed automatically as soon as possible.

To do this,

1. Log into the RemoteScope API following the instructions in [RemoteScope API Authentication](https://remotescope.netlify.app/docs/remotescope-api/api-authentication/).
2. Select which telescope to use and the configurations for your observation. See the sample API call below:

```
curl --request POST \
--url https://api.remotescope.com/v1/photos \
--header 'authorization: Bearer <<YOUR_API_KEY>>' \
--header 'content-type: application/json' \
--data'{
            "name": "Telescope Charlie",
            "target": "Andromeda",
            "timeOfCapture": 1587346996,
            "exposureTimeSeconds": "15",
            "filter": "noFilter"
}'
```