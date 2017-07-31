## Hey There
Here is the code for Unmark's Firefox extension. Feel free to use it. Below are a few instructions on how to customize it to work with your domain.

This is a slightly adopted fork of [unmark's Chrome Extension](https://github.com/plainmade/unmark-chrome) to work in Firefox.

## Using your own host
If you want to simply change the endpoint for this extension it's pretty simple.

* Open `manifest.json` and find the block that looks like:

```
"permissions": [
    "tabs",
    "contextMenus",
    "*://unmark.it/"
  ],
```

Change the last line to match your site.

* Open `js/unmark/base.js` and change line 2 to point to the correct endpoint.

```
unmark.host = 'https://unmark.it';
```

* Save

## Loading your version in Firefox
Now you should be able to load the unpacked extension locally and test. To do that simply follow these instructions:

* Go To `about:debugging` in Firefox.
* Click the button that says `Load Add-on temporary ...`.
* Choose the location of your `manifest.json`.

## Shipping your version
You can publish your version as described on [MDN web docs](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Publishing_your_WebExtension)
To create a `.xpi` file, follow the instrucions on https://developer.mozilla.org/en-US/Add-ons/Extension_Packaging (for now). You can find an example `install.rdf`-file in the project folder.