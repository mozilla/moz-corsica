moz-corsica
===========

[![Build Status](https://travis-ci.org/mozilla/moz-corsica.svg)](https://travis-ci.org/mozilla/moz-corsica)

Public Corsica instance for Mozilla office and home offices.

If you are at a Mozilla office, this project is what powers the content
on the flat screen TVs throughout the office.

Connecting a Client
-------------------

Navigate to `corsica.mozilla.io` in your web browser and you should see the Corsica logo (C with a lightning bolt). Now open the Web Console (Tools-> Web Developer-> Web Console) and run the following command:

```javascript
config.name = "location"; config.tags = ["ambient", "whimsy"]; writeConfig();
```

**Refresh the page** in your browser. Congrats! You should now start receiving content destined for the tags you set.  Go into fullscreen (type `f`) and enjoy!

### About the Name and Tag config options ###

The **name** option is the name of your screen; it can be any unique name (eg: "abby-laptop" or "matt-kitchen"). The names in the `state.json` file (eg: "pdx-ambient1") are intended for addressing multiple screens in a location.

You can choose from the following **tags** for your screen:

* `airmo` (Air Mozilla)
* `ambient`
* `mtv` (Mountain View)
* `pdx-eng` (Portland Engineering)
* `servicedesk`
* `tor` (Toronto)
* `whimsy` (Fun things!)

Most office displays are set to at least `ambient`. Because `whimsy` is fun, it's used in this example.

Development Guide
-----------------

To develop and test this project, you'll need [Node.js](https://nodejs.org/).

Bootstrap the development environment by running `script/bootstrap`.

Start a local HTTP server by running `node node_modules/corsica/index.js`.
Then, connect to the server at the address listed.

Suggesting New Content
----------------------

Want to suggest new content? Send a pull request to mozilla/moz-corsica.
