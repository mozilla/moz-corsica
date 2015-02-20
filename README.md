moz-corsica
===========

[![Build Status](https://travis-ci.org/mozilla/moz-corsica.svg)](https://travis-ci.org/mozilla/moz-corsica)

Public Corsica instance for Mozilla office and home offices.

If you are at a Mozilla office, this project is what powers the content
on the flat screen TVs throughout the office.

Connecting a Client
-------------------

Navigate to `corsica.mozilla.io` in your web browser and you should see the Corsica logo (C with a lightning bolt). Now open the Web Console (Tools-> Web Developer-> Web Console) and run the following command:

    config.name = "location"; config.tags = ["ambient", "whimsy"]; writeConfig();

Name/Tags Config: For the tag options the state.json file in this repo contains several groupings of urls tagged for various purposes. Most office displays are set to at least "ambient" but since "whimsy" is fun to have in the mix it's used in this example. You can replace "location" with any unique name (eg: "abby-laptop"), the names in the state.json file (eg: "pdx-ambient1") are intended for addressing multiple screens in a location

After you writeConfig(); you'll see the result displayed as 'undefined' and at that point reload the page. You should now start recieving content destined for the tags you set.  Go into fullscreen and enjoy!

Development Guide
-----------------

To develop and test this project, you'll need Node.js.

Bootstrap the development environment by running `script/bootstrap`.

Start a local HTTP server by running `node node_modules/corsica/index.js`.
Then, connect to the server at the address listed.

Suggesting New Content
----------------------

Want to suggest new content? Send a pull request to mozilla/moz-corsica.
