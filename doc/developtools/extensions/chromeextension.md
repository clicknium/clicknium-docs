# Chrome Extension<!-- {docsify-ignore-all} -->

**You can automate Chrome by installing the Chrome extension.**

> **Remarks:**
>
>- Official version of Chrome is recommended. The portable version or the forum customized version of the Chrome may not be well recommended.
>- The minimum Chrome version is 60.
>- Before installing the extension, please ensure the Edge is closed and no backend running msedge.exe process.

## Install

1. You can install the extension in [VSCode Clicknium Extension](./doc/developtools/vscode) or  [Clicknium Python Sdk](./doc/api/python/webdriver/webextension/webextension)

    - install the Chrome extension in [VSCode Clicknium Extension](./doc/developtools/vscode)  
        ![chrome extension install](../../img/chrome_ext_install.png)
    - install the Chrome extension in[Clicknium Python Sdk](./doc/api/python/webdriver/webextension/webextension)
    ```python
    from clicknium import clicknium as cc

    # install chrome extension
    cc.chrome.extension.install()
    ```

2. Click "OK" in below pop-up dialog box.  
    &emsp;&emsp;![chrome extension install confirm](../../img/chrome_install_confirm_dialog.png)

3. When the installation is finished, click "OK" in below pop-up dialog box.  
    &emsp;&emsp;![chrome extension install finish confirm](../../img/chrome_install_finish_dialog.png)  

4. Open extension in Chrome browser  
    4.1 Open Chrome browser and click "More Tools > Extensions" in the side navigation bar  
    &emsp;&emsp;![chrome extension page](../../img/chrome_extension_page.png)  
    4.2 In the open page, find the "Clicknium Recorder" extension.  
    &emsp;&emsp;![chrome clickniuim extension page](../../img/chrome_extension_enable_page.png)  
    4.3 Click the button "Enable" in the lower right corner of this extension.  
    &emsp;&emsp;![enable chrome clickniuim extension](../../img/chrome_extension_enable_on.png)

5. You can refer to console output for more installation details.