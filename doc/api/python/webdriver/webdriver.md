# WebDriver

**WebDriver class provides methods to getting browser object through 'open new browser' or 'attach to opened browser', and browser extension object.**

## extension <!-- {docsify-ignore} -->
- [WebExtension](./doc/api/python/webdriver/webextension/webextension.md), get web extension with different browsers by the following way, currently supporting Chrome, Edge and Firefox.   
    - import
  ```
  from clicknium import clicknium as cc
  ```
  - cc.chrome.extension: Chrome extension
  - cc.edge.extension: Edge extension
  - cc.firefox.extension: Firefox extension

## Properties <!-- {docsify-ignore} -->
- browsers: List[[Browser](./doc/api/python/webdriver/browser/browser.md)], get all open browsers by current browser type.

## methods <!-- {docsify-ignore} -->

- [open](./doc/api/python/webdriver/open.md): open the browser with specified url, and return [BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object.
- [attach](./doc/api/python/webdriver/attach.md): attach to the open browser, return [BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object.
- [attach_by_title_url](./doc/api/python/webdriver/attach_by_title_url.md): attach to the broswer with specified title or url, return [BrowserTab](./doc/api/python/webdriver/browser/browser_tab.md) object.
