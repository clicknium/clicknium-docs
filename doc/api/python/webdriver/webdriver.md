# WebDriver <!-- {docsify-ignore-all} -->

**WebDriver class provides methods to get browser object through 'open new browser' or 'attach to opened browser', and browser extension object.**

## extension
- [WebExtension](./doc/api/python/webdriver/webextension/webextension.md), get web extension with different browsers by the following way, currently supporting Chrome, Edge and Firefox.   
    - import
  ```
  from clicknium import clicknium as cc
  ```
  - cc.chrome.extension: Chrome extension
  - cc.edge.extension: Edge extension
  - cc.firefox.extension: Firefox extension

## properties
- browsers: List[[Browser](./doc/api/python/webdriver/browser/browser.md)], get all open browsers by current browser type.

## methods

- [open](./doc/api/python/webdriver/open.md): open browser with specified url to get a browser tab, return [BrowserTab](./doc/api/python/webdriver/browser/browsertab/browser_tab.md) object
- [attach](./doc/api/python/webdriver/attach.md): attach to an opened browser tab with specified locator, return [BrowserTab](./doc/api/python/webdriver/browser/browsertab/browser_tab.md) object
- [attach_by_title_url](./doc/api/python/webdriver/attach_by_title_url.md): attach to an opened browser tab with specified title and/or url, return [BrowserTab](./doc/api/python/webdriver/browser/browsertab/browser_tab.md) object
