# Firefox Extension<!-- {docsify-ignore-all} -->

**You can automate Firefox by installing the Firefox extension.**

> **Remarks:**
>
>- The minimum Firefox version is 56.
>- Before installing the extension, please ensure the Firefox is closed.

## Install

1. You can install the extension in [VSCode Clicknium Extension](./doc/developtools/vscode) or [Clicknium Python Sdk](./doc/api/python/webdriver/webextension/webextension)

    - install the extension in [VSCode Clicknium Extension](./doc/developtools/vscode)  
        ![firefox extension install](../../img/firefox_ext_install.png)
    - install the extenion in [Clicknium Python Sdk](./doc/api/python/webdriver/webextension/webextension)
    ```python
    from clicknium import clicknium as cc

    # install firefox extension
    cc.firefox.extension.install()
    ```

2. Click "OK" in below pop-up dialog box.  
    &emsp;&emsp;![firefox extension install confirm](../../img/firefox_install_confirm_dialog.png)

3. When the installation is finished, click "OK" in below pop-up dialog box.  
    &emsp;&emsp;![firefox extension install finish confirm](../../img/firefox_install_finish_dialog.png)  

4. Open extension in Firefox 
    Open firefox browser and in the open page, find the "Clicknium Recorder" extension, and add it.  
    &emsp;&emsp;![firefox clickniuim extension page](../../img/firefox_extension_enable_on.png)

5. You can refer to console output for more installation details.