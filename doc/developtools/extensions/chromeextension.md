# Chrome Extension<!-- {docsify-ignore-all} -->

**You can automate Chrome by installing the Chrome extension.**

> **Remarks:**
>
>- Official version of Chrome is recommended. The portable version or the forum customized version of the Chrome may not be well supported.
>- The minimum Chrome version is 60.
>- Please close Chrome browser before installing the extension.

## Install

1. You can install the extension in two ways:  
    - Install the Chrome extension in [VSCode Clicknium Extension](./doc/developtools/vscode)  
        ![chrome extension install](../../img/chrome_ext_install.png)
    - Install the Chrome extension via [Clicknium Python command](./doc/api/python/webdriver/webextension/webextension)
    ```python
    from clicknium import clicknium as cc

    # install chrome extension
    cc.chrome.extension.install()
    
2. Enable extension in Chrome browser  
    - Open Chrome browser and click "More Tools > Extensions" in the side navigation bar  
    &emsp;&emsp;![chrome extension page](../../img/chrome_extension_page.png)  
    - In the open page, find the "Clicknium Recorder" extension.  
    &emsp;&emsp;![chrome clickniuim extension page](../../img/chrome_extension_enable_page.png)  
    - Click the button "Enable" in the lower right corner of this extension.  
    &emsp;&emsp;![enable chrome clickniuim extension](../../img/chrome_extension_enable_on.png)

3. You can refer to console output for more installation details.