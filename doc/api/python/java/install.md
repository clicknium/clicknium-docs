# install

***def install(self, java_install_path: str = '') -> None*** 

Install java extension.

>**Remarks:**  
>- Make sure you have installed java or jre.

**Parameters:**  
    &emsp;**java_install_path**: str  
        &emsp;&emsp; The java installation path, like "C:\\Program Files\\Java\\jdk-17.0.2\\bin". The system will try to find it under "Program Files && Program Files (x86)" if this parameter is not specified.

**Returns:**  
    &emsp;None

**Example:**
***
```python
    from clicknium import clicknium as cc

    # get java driver
    java_driver = cc.java

    # install java extension with default java install path "Program Files && Program Files (x86)"
    java_driver.extension.install()

    # install java extension with specified java install path
    java_driver.extension.install(java_install_path = "C:\\Program Files\\Java\\jdk-17.0.2\\bin")

```