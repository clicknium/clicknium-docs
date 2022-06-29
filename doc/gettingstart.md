# Getting started<!-- {docsify-ignore-all} -->

- [Getting started](#getting-started)
- [Installation​](#installation)
  - [System Requirements​](#system-requirements)
  - [Install Clicknium Visual Studio Code extension](#install-clicknium-visual-studio-code-extension)
  - [Install Clicknium python package](#install-clicknium-python-package)
- [Create project](#create-project)
- [Install and enable browser extension](#install-and-enable-browser-extension)
- [Run/debug the project](#rundebug-the-project)
- [Record UI Locators](#record-ui-locators)
- [Edit and Validate Locator](#edit-and-validate-locator)
- [Documents Guideline](#documents-guideline)

[ClickCorp](https://www.clickcorp.com) builds a new generation automation framework **Clicknium** to support GUI automation for all types of applications. Automation development efficiency is highly improved with features of Clicknium, including developer tooling support and cloud native data management for colaboration.  

[Clicknium Python Package](./doc/api/python/pythonsdk.md): Clicknium python package provides programming interfaces to automate various types of applications, such as Web browser, Windows Desktop application, Java application and Sap windows Gui app, etc.  
(If other programming languages support are required, please [contact us](https://www.clickcorp.com/contact).)  

[Clicknium Visual Studio Code Extension](./doc/developtools/vscode.md): This extension helps you capture and manage UI locators easily. Unlike selenium or playwright that you need to figure out the locators by XPath or CssSelector. Clicknium extension generates locators by just clicking the target UI element, with [Clicknium Python Package](https://pypi.org/project/clicknium/), you can start automation for web and desktop right away. Besides generating locators automatically, Clicknium also provides locator IntelliSense in coding, centralized locator management in cloud, and project distribution.  

# Installation​
## System Requirements​
- Windows 7 SP1 or above
- Python 3.7 or above

## Install Clicknium Visual Studio Code extension
Click the following link to install [Clicknium Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=ClickCorp.clicknium). After installation, you are required to sign in ClickCorp.  
![login](https://clickcorp.github.io/clicknium-docs/doc/img/login1.png "login")  
Click 'Allow' to sign in ClickCorp, or sign in with a Google or GitHub account.

## Install Clicknium python package
If you didn't have python environment, please refer to [Python in Visual Studio Code](https://code.visualstudio.com/docs/languages/python).  
To install Clicknium python package, you can follow the steps as below:  

```
# python version is 3.8 or below
pip install clicknium

# python version is 3.9 or above
pip install --pre pythonnet
pip install clicknium
```

# Create project
- In Visual Studio Code, open the Command Palette: `Ctrl+Shift+P`
- Input or select: `Clicknium: Create Clicknium Project`
- Select 'Sample Project'  
![project type](https://clickcorp.github.io/clicknium-docs/doc/img/project_type.png)  
- Select project path, you can create one empty folder and select it
  
Then project is created with a default locator store `new_store`.  

![locator ref](https://clickcorp.github.io/clicknium-docs/doc/img/locator_ref.png "locator ref")  

The default project contains two automation samples, one is Edge web automation, and another is notepad automation.
```python
import subprocess
from time import sleep
from clicknium import clicknium as cc, locator, ui


def main():
    # sample code to demo web automation and desktop application
    tab = cc.edge.open("https://www.bing.com/")
    tab.find_element(
        locator.new_store.sample.bing.search_sb_form_q).set_text('clicknium')
    tab.find_element(locator.new_store.sample.bing.svg).click()
    sleep(3)
    tab.close()

    process = subprocess.Popen("notepad")
    ui(locator.new_store.sample.notepad.document_15).set_text("clicknium")

if __name__ == "__main__":
    main()
```

# Install and enable browser extension
Click 'Clicknium Explorer' in Visual Studio Code Activity Bar.  
Show 'AUTOMATION EXTENSIONS' view in Visual Studio Code Side Bar.  
Choose the Edge browser and click the 'install' button.  
After installation, you need to open Edge browser to enable 'Clicknium Recorder' extension.  

![enable edge extension](https://clickcorp.github.io/clicknium-docs/doc/img/edge_extension_enable_on.png)  

# Run/debug the project
- Via Visual Studio Code built in commands:
  - `F5` to debug project
  - `Ctrl+F5` to run project
- Via Command Palette (`Ctrl+Shift+P`):
  - `Clicknium: Debug Project` to debug project
  - `Clicknium: Run Project` to run project

# Record UI Locators
In Visual Studio Code, press `Ctrl+F10` will invoke Clicknium Recorder and minimize current Visual Studio Code window.  
![clicknium recorder](https://clickcorp.github.io/clicknium-docs/doc/img/recorder_main.png)

After invoking Clicknium Recorder, you can hover the mouse over the target application to highlight the element recognized. 
If you want to capture the element, press `Ctrl` and click the element to generate locator and add to store.

# Edit and Validate Locator
After recording the locators, you can open and edit the locator  
![clicknium Visual Studio code](https://clickcorp.github.io/clicknium-docs/doc/img/main.png) 

# Documents Guideline
For more about Clicknium Visual Studio Code, please refer [here](/doc/developtools/vscode.md).  
You may need to refer [Clicknium python package documents](/doc/api/python/pythonsdk.md) when writing code.  
For more tools provided by Clicknium, please refer to:  
- [Clicknium Recorder](/doc/developtools/recorder.md).  
- Clicknium Browser Extension: [Chrome](/doc/developtools/extensions/chromeextension.md), [Edge](/doc/developtools/extensions/edgeextension.md), [Firefox](/doc/developtools/extensions/firefoxextension.md).  
- [Clicknium Java Extension](/doc/developtools/extensions/javaextension.md).  
