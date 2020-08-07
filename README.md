# Create-Chrome-Extension

## Why does this repo exist?

Chrome extensions are yet another way to solve problems with technology. This repository is meant for engineers who want to quickly get started and start chewing bubble gum.
Jules Patry is the creator of this repository.

## Getting started

[Google's docs for getting started with chrome extensions.](https://developer.chrome.com/extensions/getstarted)

The first place to look to understand a Chrome extension is the `manifest.json` file.

```
{
  "name": "Create Chrome Extension",
  "version": "1.0",
  "description": "Starter kit for creating a chrome extension. Great for those who are trying different approaches to chrome extensions.",
  "permissions": ["storage"],
  "background": {
    "scripts": ["background.js"],
    "persistent": false
  },
  "page_action": {
    "default_popup": "popup.html"
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

[For more reference on background.js, click here](https://developer.chrome.com/extensions/background_pages)

[Click here, for `chrome.runtime`'s API.](https://developer.chrome.com/extensions/runtime#event-onInstalledhttps://developer.chrome.com/extensions/runtime#event-onInstalled)

## Permissions

The `permission` key in the `manifest.json` file is a property reserved to access chrome's API's such as local storage or the tabs of a browser.

[Here is the list of chrome's API](https://developer.chrome.com/extensions/api_index)
