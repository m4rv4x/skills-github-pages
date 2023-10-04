---
title: "current-city"
date: 2023-10-04
---

To know your current city using the `curl` command in the command line interface (CLI), you can make use of a geolocation API service. One popular service is the ipapi API, which provides geolocation data based on IP addresses.

Here's an example command to retrieve your current city using `curl` and the ipapi API:

```bash
curl -s 'https://ipapi.co/json/' | jq -r '.city'
```

This command sends a GET request to the ipapi API endpoint and retrieves the JSON response. The `jq` command-line tool is then used to extract the city value from the JSON response.

Make sure you have `jq` installed on your system before running the command. If it's not installed, you can install it using the package manager for your Linux distribution.

Note: The accuracy of the geolocation data depends on the IP address assigned to your system by your internet service provider (ISP).
