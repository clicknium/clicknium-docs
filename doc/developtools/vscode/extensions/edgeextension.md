---
sidebar_position: 2
sidebar_label: Edge Extension
---
# Microsoft Edge Extension

**You can automate Edge by installing the Microsoft Edge extension.**

> **Remarks:**
>
>- Please close the Edge browser and ensure no msedge.exe process is running before installing this extension.

## Install

1. You can install the extension in two ways:
    - Install the extension in [VSCode Clicknium Extension](./../vscode.md)  
        ![edge extension install](../../../img/edge_ext_install.png)
    - Install the extension via [Clicknium Python command](./../../../references/python/webdriver/webextension/webextension.md)
    ```python
    from clicknium import clicknium as cc

    # install edge extension
    cc.edge.extension.install()
    ```
2. Enable the extension in Edge  
    - Open Edge and click "Extensions" in the side navigation bar  
    &emsp;&emsp;![edge extension page](../../../img/edge_extension_page.png)  
    - In the open page , find the "Clicknium Recorder" extension.  
    &emsp;&emsp;![edge clickniuim extension page](../../../img/edge_extension_enable_page.png)  
    - Click the button "Enable" in the lower right corner of this extension.  
    &emsp;&emsp;![enable edge clickniuim extension](../../../img/edge_extension_enable_on.png)

3. You can refer to console output for more installation details.