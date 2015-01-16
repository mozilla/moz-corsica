moz-corsica
===========

[![Build Status](https://travis-ci.org/mozilla/moz-corsica.svg)](https://travis-ci.org/mozilla/moz-corsica)

Public Corsica instance for Mozilla office and home offices. Use Pull Requests to suggest new content.

Connecting a Client
-------------------

Once you connect to `corsica.mozilla.io`, you should see the Corsica logo (C with a lightning bolt). Open the browser console and run the following commands, substituting the values as necessary for your installation:

    config.name = "location#";
    config.tags = ["ambient", "whimsy"];
    writeConfig();

Refresh the page and you should be recieving content destined for those tags or that specific name.

TODO:

1. overview
2. how to contribute
3. content guide
4. put all this in a wiki maybe?
