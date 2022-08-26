# Change Log
## 0.1.5 (26 August 2022)
### New features
- New api: support mouse emulation events, clicknium.mouse.click/double_click/up/down/move/scroll/positon.
- Support turning on browser extensions for chrome and edge automatically. 
- Support validation elements with specified index.
- Support attribute `name` for UIA locator.

### Improvements
- Optimize the default names for locators.
- Refactor JAVA automation, optimize automation on JAVA applications.
- Fix bug: clicknium module can not run on Windows 7.
- Fix bug: automating browsers may get errors when opening browsers concurrently.
- Fix bug: locating elements may get errors with the default value for attribute `index`.
- Fix bug: recording elements may get errors when other browsers' extensions running.

## 0.1.4 (12 August 2022)
### New features
- New api: BrowserTab.scroll(delta_x, delta_y), scroll the current browser tab with the scroll bar.
- New api: WebElement.scroll(delta_x, delta_y), scroll the current web element with the scroll bar.
- Support regular expression operator in the locator.
- Support automation for explorer appbar control on windows 11.
- Update the requirements of clicknium python module. With the python version greater than 3.9(include 3.9), pythonnet module will be installed by default.

### Improvements
- Improve the attach error for the browser tab when the browser extension is not ready.
- Improve the experience of recording the similar elements.
- Improve the performance of Clicknium Recorder.
- Improve UI button style for Clicknium Recorder.
- Fix bug: record 'svg' element failed with error "Unexpected character encountered while parsing value: 'responseData.htmlAttributes.class'".
- Fix bug: `find_elements` must wait until the web page has been loaded.
- Fix bug: `set_text` can not work when the text is a number.
- Fix bug: remind users if there are a number of Chrome windows with various user profiles, recording fails.

## 0.1.3 (1 August 2022)
### New features
- New api: clicknium.edge/chrome/firefox.extension.is_installed(), check whether the extension is installed.
- Updated api: add `with` function for browsertab class.
- Updated locator: support 'class' and 'ancestorclass' attribute in locator of web automation.

### Improvements
- Improve browser extension installation experience.
- Fix web automation bug: validation failed for web element with `tabIndex` property.
- Fix bug: can not get actual element's rectangle, when window's DPI changed.
- Fix bug: new_tab was not working when url does not start with `https://`,`http://` or `file://`.
- Fix bug: open browser can not get correct tab id when there is some other popup window.
- Fix bug: send_hotkey does not support some modifier keys, such as '^' (for ctrl).

## 0.1.2 (19 July 2022)
### New features
- New API: new_tab on browser class.
- New API: clicknium.edge/chrome/firefox.extension.detect(), it can get the installation state of the browser extension. 
- New API: clicknium.edge/chrome/firefox.extension.install_or_update(), it will install brower extension when extension is not installed or has a newer version.
- New API: get_screenshot, global interface to capture the screenshot.
- Updated API: set_text with new parameter `overwrite`, indicate whether overwrite the text or append the text on the target element.

### Improvements
- Fix yrate not working issue for API click, double_click.
- Improve browser extension installation experience.
- The front active window will be selected when there are multiple windows matched by given locator during automation run.
- Fix UIA bug: validation failed on navigation pane of windows file explorer.
- Improve locator for web automation: trim the space for the value of attribute sinfo, name etc.
- Fix web automation bug: modifier_key was not working on web element.
- Improve recording element experience on SAP to ensure the generated locator is SAP specific.

## 0.1.0 (30 June 2022)
Initial release version.
- Several desktop automation libraries: UIA, Java, IA, SAP automation.
- Several web automation libraries: Chrome, Edge, Internet Explorer(IE), FireFox.
- Support automation based on image recognization.
- Unified automation API for different applications, such as click, set_text, get_text, send_hotkey, select_item etc.
- Special APIs for web automation: open browser, attach to already opened browser, get active tab, close browser, refresh tab, close tab etc.
- Special API for application window: maximize, minimize, restore etc.
- Special API for SAP windows GUI application: login, call_transaction, get_statusbar etc.
- API to install chrome/edge/firefox browser extension.
