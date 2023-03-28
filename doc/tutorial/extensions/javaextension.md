---
sidebar_position: 4
---
# Java Extension

**Java Extension is applicable to the automation of Java 1.6 and greater but below Java 9 applications.**

> **Remarks:**
>
> For applications opened with Java 9+ JRE:
>- Prior to Java 9, JRE included the attach module, which Java Extension relies on to automate Java applications.
>- For Java 9+, the attach module is only included in JDK. For applications opened with JRE9+, you need to manually add this module under the JRE directory.
>- Before installing the extension, please close all Java applications.

## Installation

1. You can install the extension in two ways:

    - Install the extension in [VSCode Clicknium Extension](./../../tutorial/vscode/vscode.md)  
        ![java extension install](../../img/java_ext_install.png)

    - Install the extension via [Clicknium Python command](./../../references/python/java/java.md)
    ```python
    from clicknium import clicknium as cc

    # install java extension
    cc.java.extension.install()
    ```

2. Click "Yes" on the User Account Control window to start the installation.  
   &emsp;&emsp;![java install admin confirm](../../img/java_extension_admin_confirm.png)


3. Refer to the console output for more installation details. Please note that the Java extension status will `not change` in VS Code extension since multiple JRE/JDK environments could exist.   
![](../../img/java_ext_install_finish.png)

### To double check the installation status:  
 Go to `{JRE}/lib/accessibility.properties,` and check the file contents to see if the Clicknium settings exist or not.   
 ![](../../img/java_extension_check.jpg)