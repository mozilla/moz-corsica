# Adding Content to Corsica

1. Content should be “10 foot” readable. This means larger font-size, coarser details. Office screens are 1920x1080 and are generally mounted ~6 feet off the ground.

2. Content should be reachable via the *public internet*- the office TVs are really just a bunch of networked `<iframe>` tags, and are orchestrated via a public server. The general rule for office TVs is that they are in public space, so don’t put any information on them you wouldn’t want a random passer-by to see.

3. Content must be able to be `<iframe>`d. This means if the site in question has an `X-Frame-Options: Deny` header or other frame-busting code, it will not work on the TVs. If you’re building something custom, this shouldn’t really be a problem, but comes up when trying to use third-party tools.

4. No animation. Some very basic “loading” spinner at the beginning is fine, but these TVs are frequently placed in areas where people are trying to get work done, and constant motion is very distracting. We’ve tried having animation, and people walk over and turn the TVs off. Engineers are particular about this bit.

5. Load reasonably quickly. Content on the TVs cycles approximately once every two minutes. If the page spends 30+ seconds fetching and processing data, the data will not be on the screens very long. Most dashboards are built with a small node caching server that fetches the data every few minutes, and can serve the cached data immediately to a dashboard that requests it.
