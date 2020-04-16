---
title: "Authentication"
date: 2020-03-27
weight: 2
description: >
  Instructions how to authenticate to the RemoteScope API
---

{{% pageinfo %}}
RemoteScope uses [Oauth2](http://oauthbible.com/#oauth-2-three-legged) for authentication to the API. Read this page to learn how to get a user token and authenticate.
{{% /pageinfo %}}

Before you can start using the API, you need to do the following:

1. Create a RemoteScope account.
2. Create an API Key.
3. Make sure you have [curl](https://curl.haxx.se/) installed on your machine.



## Take a first photo using the RemoteScope API
To take a first photo using the RemoteScope API:

```
curl --request POST \
--url https://api.remotescope.com/v1/photos \
--header 'authorization: Bearer <<YOUR_API_KEY>>' \
--header 'content-type: application/json' \
--data'{
            "name": "Telescope Charlie",
            "target": "Andromeda",
            "exposureTimeSeconds": "15",
            "filter": "noFilter"
}'
```

1. Copy the curl example above.
2. Paste the curl call into your favorite text editor.
3. Copy your API key and paste it in the authorization header.
4. Copy the code and paste it in your terminal.
5. Hit Enter.

Check your inbox of the address connected to your RemoteScope account and see your message!

