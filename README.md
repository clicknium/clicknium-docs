<!--
 Licensed to the Apache Software Foundation (ASF) under one
 or more contributor license agreements.  See the NOTICE file
 distributed with this work for additional information
 regarding copyright ownership.  The ASF licenses this file
 to you under the Apache License, Version 2.0 (the
 "License"); you may not use this file except in compliance
 with the License.  You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing,
 software distributed under the License is distributed on an
 "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
 KIND, either express or implied.  See the License for the
 specific language governing permissions and limitations
 under the License.
-->

[![PyPI version](https://badge.fury.io/py/Clicknium.svg)](https://badge.fury.io/py/Clicknium)
[![GitHub issues](https://img.shields.io/github/issues/clicknium/clicknium-docs)](https://github.com/clicknium/clicknium-docs/issues)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/clicknium?style=flat-square)
[![Twitter URL](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Ftwitter.com%2Fclicknium)](https://twitter.com/clicknium)
[![Slack Status](https://img.shields.io/badge/slack-join_chat-white.svg?logo=slack&style=social)](https://join.slack.com/t/clicknium/shared_invite/zt-1gi6v3d85-8sBgen83vD6EhL48UEhxwQ)

# Clicknium-docs

[Clicknium](https://www.clicknium.com) is a next-generation GUI automation framework for various types of applications. It offers a simple and streamlined developer experience with high-level APIs for automating GUI applications and intelligent plug-ins. It gives you a fresh approach to creating your automation universe. Browser automation, web and desktop application testing, and site scraping bots are also supported.
## Requirements
|                     | Main version                 | 
|---------------------|------------------------------|
| Python              | 3.7, 3.8, 3.9, 3.10          | 
| OS                  | Windows 11, 10 recommended, Windows 7 SP1 or above|
>Note: Windows 10 is the minimum supported Windows OS for DPI awareness.    

### Code Editor
- Visual Studio Code

## Getting Started

Get a sample script showing automation of web page and notepad.

## Installation​
### Set Up Clicknium Visual Studio Code Extension
1. Install the [Extension](https://marketplace.visualstudio.com/items?itemName=ClickCorp.clicknium) (or search `Clicknium` in Visual Studio Code Extension marketplace).  
![VSCExtensions](./doc/img/vscextension.PNG)  
2. Click `CLICKNIUM EXPLORER` in Visual Studio Code Activity Bar
3. Follow the welcome page:
    - Check the Python environment.
    - Install Clicknium Python module, as well as `pip install clicknium`
    - Select and install the browser extensions, at least including Edge. Enable the extension after the installation. 
    - Sign in to start for free.   
    
    ![welcomepage](./doc/img/vscwelcome.PNG)

_To Reopen Welcome Page: open the Command Palette: Ctrl+Shift+P, input `Clicknium:Welcome`_

_To Enable Edge Extension: Open Edge browser, type `edge://extensions/` into the address bar and enable `Clicknium Recorder` extension as below:_

![enable edge extension](./doc/img/edge_extension_enable_on.png)  


### Setup Sample Project
- Click `Clicknium: Sample` on Welcome Page. Or invoke the Command Palette by pressing Ctrl+Shift+P and inputting `Clicknium:` Sample`.
- Choose a path to locate the sample project.

The sample.py contains two automation samples, one is Edge web automation, and the other is notepad automation.

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
    sleep(3)

if __name__ == "__main__":
    main()
```

### Run the Sample
In Visual Studio Code, open sample.py and press `Ctrl+F5` to run the script. It will do: 
- Open a search engine page
- Input a keyword and click the search button
- Open a notepad
- Input text to notepad

## Next 
Learn [how to start an automation project from zero](./doc/tutorial/firstautomation.md).

## Contact
Welcome to create a [Github Issue](https://github.com/clicknium/clicknium-docs/issues) or join [Clicknium Slack](https://clicknium.slack.com/) if you have any questions.