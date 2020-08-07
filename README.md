# Create-Chrome-Extension

## Why does this repo exist?

This repository's purpose is for engineers who want to quickly develop and chew bubble gum.

Jules Patry is the creator of this repository.

## Getting started

[Google's docs for getting started with chrome extensions.](https://developer.chrome.com/extensions/getstarted)

The first place to look to understand a Chrome extension is the `manifest.json` file.

```
{
  "name": "Create Chrome Extension",
  "version": "1.0",
  "description": "Starter kit for creating a chrome extension. Great for those who are trying different approaches to chrome extensions.",
  "permissions": ["declarativeContent", "storage"],
  "background": {
    "scripts": ["background.js"],
    "persistent": false
  },
  "page_action": {
    "default_popup": "popup.html",
    "default_icon": {
      "16": "images/test-16.png",
      "32": "images/test-32.png",
      "48": "images/test-48.png",
      "128": "images/test-128.png"
    }
  },
  "icons": {
    "16": "images/test-16.png",
    "32": "images/test-32.png",
    "48": "images/test-48.png",
    "128": "images/test-128.png"
  },
  "manifest_version": 2
}

```

## Background Listeners

In the `manifest.json` file there is a property called background which takes an array of file names. `background.js` will be used to listen to certain events such as executing endpoints or changing the html.

Below is a snippet from the Chrome Docs.

```
Extensions are event based programs used to modify or enhance the Chrome browsing experience. Events are browser triggers, such as navigating to a new page, removing a bookmark, or closing a tab. Extensions monitor these events in their background script, then react with specified instructions.
```

In this repo, `background.js` saves a color variable to the local storage. It has access to local storage because of the permissions key, more noted below.

[For more reference on background.js, click here](https://developer.chrome.com/extensions/background_pages)

[Click here, for `chrome.runtime`'s API.](https://developer.chrome.com/extensions/runtime#event-onInstalledhttps://developer.chrome.com/extensions/runtime#event-onInstalled)

## Permissions

The `permission` key in the `manifest.json` file is a property reserved to access chrome's API's such as local storage or the tabs of a browser.

[Here is the list of chrome's API](https://developer.chrome.com/extensions/api_index)

## page_action

`page_action` is the ui of the chrome extension which in this repository's case is `popup.js`. Note that `popup.js` has a script tag sourcing to `popup.js` which simply access the local storage for a color that was set in `background.js`.

## More Examples!

[For more examples of chrome extensions, check here!](https://developer.chrome.com/extensions/samples#page-redder)
