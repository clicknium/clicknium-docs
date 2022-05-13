# WebDriver

**WebDriver class provides methods to get browser object through 'open new browser' or 'attach to opened browser', and get browser extension object.**

## extension <!-- {docsify-ignore} -->
- [WebExtension](./doc/api/python/webdriver/webextension/webextension.md), through the following way can get web extension for different browser type, current support chrome, edge, firefox.   
    - import
  ```
  from clicknium import clicknium as cc
  ```
  - cc.chrome.extension: chrome extension
  - cc.edge.extension: edge extension
  - cc.firefox.extension: firefox extension

## methods <!-- {docsify-ignore} -->

- [open](./doc/api/python/webdriver/open.md): open browser with specified website, return [Browser](./doc/api/python/webdriver/browser/browser.md) object
- [attach](./doc/api/python/webdriver/attach.md): attach to opened browser, return [Browser](./doc/api/python/webdriver/browser/browser.md) object