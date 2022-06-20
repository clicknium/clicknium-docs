# Getting started<!-- {docsify-ignore-all} -->

- [Getting started](#getting-started)
  - [Overview](#overview)
  - [Installation​](#installation)
    - [System Requirements​](#system-requirements)
    - [Install Clicknium Visual Studio Code extension](#install-clicknium-visual-studio-code-extension)
- [First project](#first-project)
- [Record UI Locators](#record-ui-locators)
- [Edit and Validate Locator](#edit-and-validate-locator)
- [Manually Install Clicknium Python SDK](#manually-install-clicknium-python-sdk)
- [Documents Guideline](#documents-guideline)

## Overview

[ClickCorp](https://wwww.clickcorp.com) builds an open-source automation stack for developers to write software robot projects, and hosts cloud native approach products for software robot running and managment. Automation stack includes the following main parts: 

[Clicknium Python SDK](./doc/api/python/pythonsdk.md): Clicknium python sdk provides methods to automate various applications, such as Web browser, Windows Desktop application, Java application, Sap windows Gui app, etc.  
Currently we provide Python SDK. If other programming languages are required, please [contact us](https://www.clickcorp.com/community)

[Clicknium Visual Studio Code Extension](./doc/developtools/vscode.md): This extension helps you capture and manage UI locators easily. Unlike selenium or playwright that you need to figure out the locator by XPath or CssSelector. Clicknium extension generates locator by just clicking the target UI element, with [Clicknium Python SDK](https://pypi.org/project/clicknium/), you can start automation for web and desktop right away. Besides generating locators automatically, it also provides locator intellisense in coding, centralized locator management in cloud, and project for distribution.

## Installation​
### System Requirements​
- Python 3.7 or above
- Windows 7 SP1 or above

### Install Clicknium Visual Studio Code extension
Click the following link to install [Clicknium Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=ClickCorp.clicknium).
After installation, you are required to sign in ClickCorp.  
![login](https://clickcorp.github.io/clicknium-docs/doc/img/login1.png "login")  
Click 'Allow' to sign in ClickCorp, or sign in with a Google or GitHub account.

# First project
- Install browser extension
  Click 'Clicknium Explorer' in VS Code Activity Bar
  Show 'AUTOMATION EXTENSIONS' view in VS Code Side Bar
  Choose the Edge browser and click the 'install' button

- In Visual Studio Code, Open the Command Palette: `Ctrl+Shift+P`
- Input or select: `Clicknium: Create Clicknium Project`
- Select project path, you can create one empty folder and select it
  
When a project is created, python virtual enviroment is created automatically, and Clicknium Python SDK is automatically installed in the virtual environment.  
You need refer to the cloud locator first:
Click 'Clicknium Explorer' in VS Code Activity Bar
Show 'CLOUD LOCATORS' view in VS Code Side Bar, click the 'reference' button on the right side of the locator store  
![locator ref](https://clickcorp.github.io/clicknium-docs/doc/img/locator_ref.png "locator ref")  

The default project contains two automation samples, one is Edge web automation, and another is notepad automation.
```
from clicknium import clicknium as cc, locator, ui

def web_automation_demo():
  tab = cc.edge.open("https://www.bing.com/")
  tab.find_element(locator.new_store.bing.search_sb_form_q).set_text('clicknium')
  tab.find_element(locator.new_store.bing.svg).click()

  result_elements = tab.find_elements(locator.new_store.bing.a_search_result)
  for elem in result_elements:
    print(elem.get_text())
    elem.highlight(duration=1)

  tab.close()
```
```
from clicknium import clicknium as cc, locator, ui
import subprocess

def desktop_automation_demo():
  process = subprocess.Popen("notepad")
  ui(locator.new_store.notepad.document_15).set_text("clicknium")
  ui(locator.new_store.notepad.document_15).clear_text('controlclearvalue')
  process.kill()
```

- Run/debug the project
You can debug through `F5` or run through `Ctrl+F5`  
or Open the Command Palette: `Ctrl+Shift+P`:
Input or select: `Clicknium: Run` to run project or `Clicknium: Debug` to debug project


# Record UI Locators
In Visual Studio Code, press `Ctrl+F10` will invoke Clicknium Recorder and minimize current Visual Studio Code window.  
![clicknium recorder](https://clickcorp.github.io/clicknium-docs/doc/img/recorder_main.png)

After invoking Clicknium Recorder, you can hover the mouse over the target application to highlight the element recognized. 
If you want to capture the element, press `Ctrl` and click the element to generate locator and add to store.

# Edit and Validate Locator
After recording the locators, you can open and edit the locator  
![clicknium VS code](https://clickcorp.github.io/clicknium-docs/doc/img/main.png) 

# Manually Install Clicknium Python SDK
If you want to manually install Clicknium Python SDK, you can follow the steps as below:
Install Clicknium automation sdk through [pip](https://pypi.org/project/clicknium/)  

```
# python version is 3.8 or below
pip install clicknium

# python version is 3.9 or above
pip install --pre pythonnet
pip install clicknium
```

# Documents Guideline
For more about Clicknium Visual Studio Code, please refer to [here](/doc/developtools/vscode.md).  
You may need to view [Clicknium Python SDK API doucments](/doc/api/python/pythonsdk.md) when writing code.
For more tools provided by Clicknium, please refer to:
[Clicknium Recorder](/doc/developtools/recorder.md)
Clicknium Browser Extension: [Chrome](/doc/developtools/extensions/chromeextension.md), [Edge](/doc/developtools/extensions/edgeextension.md), [Firefox](/doc/developtools/extensions/firefoxextension.md).  
Clicknium Java Extension: [Java](/doc/developtools/extensions/javaextension.md).  

