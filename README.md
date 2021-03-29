moz-corsica
===========

![Build Status](https://github.com/mozilla/moz-corsica/actions/workflows/ci.yml/badge.svg)

Public Corsica instance for Mozilla office and home offices.

If you are at a Mozilla office, this project is what powers the content
on the flat screen TVs throughout the office.

Suggesting New Content
----------------------

Want to suggest new content? Please file an issue, email the maintainers directly, or open a pull request to `mozilla/moz-corsica` that modifies the `state.json` file.


Connecting a Client
-------------------

Navigate to `corsica.mozilla.io` in your web browser and you should see the Corsica logo (C with a lightning bolt) and a message saying "I am *a name*". File an issue on this repository or email the maintainers directly with the following:

- [ ] the name of the screen
- [ ] where it's physically located
- [ ] what content should be on it
- [ ] any other special requests

and we can remotely configure the screen.

Alternatively, you can manually configure a window by open the Web Console (Tools-> Web Developer-> Web Console) and run the following commands, substituting your preferred values for name and tags:

```javascript
config.name = "$the-desired-name";
config.tags = ["ambient"];
writeConfig();
```

**Refresh the page** in your browser. Congrats! You should see it identify as the name you set, and start receiving content destined for the tags.  Go into fullscreen mode (type `f`) and enjoy!

### About the Name and Tag config options ###

The **name** option is the name of your screen; it can be any unique name (eg: "abby-laptop" or "matt-kitchen"). The names in the `state.json` file (eg: "pdx-ambient1") are intended for addressing multiple screens in a location.

You can choose from the following **tags** for your screen:

* `airmo` (Air Mozilla)
* `ambient`
* `mtv` (Mountain View)
* `paris`
* `pdx-eng` (Portland Engineering)
* `servicedesk`
* `tor` (Toronto)
* `whimsy` (Fun things!)
* `ldn` (London)
* `yvr` (Vancouver)
* `tpe` (Taipei)
* `tpe-lab` (Taipei Hasal Lab)

Most office displays are set to at least `ambient`, and often also `whimsy`.

Development Guide
-----------------

To add features to Corsica itself, you probably want to work on `mozilla/corsica`.

To develop and test this project, you'll need [Node.js](https://nodejs.org/).

Bootstrap the development environment by running `script/bootstrap`.

Start a local HTTP server by running `node node_modules/corsica/index.js`.
Then, connect to the server at the address listed.
