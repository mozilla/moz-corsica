moz-corsica
===========

[![Build Status](https://travis-ci.org/mozilla/moz-corsica.svg)](https://travis-ci.org/mozilla/moz-corsica)

Public Corsica instance for Mozilla office and home offices. Use Pull Requests to suggest new content.

Connecting a Client
-------------------

Navigate to `corsica.mozilla.io` in your web browser and you should see the Corsica logo (C with a lightning bolt). Now open the web console (Tools-> Web Developer-> Web Console) and run the following command, substituting the values in the tags array as necessary for your desired screen content (see state.json for options):

    config.name = "location#"; config.tags = ["ambient", "whimsy"]; writeConfig();

Refresh the page and you should start recieving content destined for those tags.  Now go to fullscreen and enjoy!

TODO:

1. overview
2. how to contribute
3. content guide
4. put all this in a wiki maybe?
