---
sidebar_position: 5
sidebar_label: Install Bowser Extension
---

# How to Install Bowser Extension

## Introduction
Since manifest V2 support ends in June of 2023 for all Chromium-based browsers. We have upgraded Chrome and Edge browser extensions from manifest V2 to manifest V3.

## Scenario
When you install clicknium extenison [online](https://chrome.google.com/webstore/detail/clicknium-recorder/ifnedcgcleipmmolmnhoeemmjnljjgna), and get the error "Unable to communicate with Clicknium native message host." from the popup window, you can try below two ways to install Clicknium native message host.

![popup window](./img/unable_to_connect_message_host.png)

## Two ways to install browser extension

### Version Requirement
[Clicknium Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=ClickCorp.clicknium) >= 0.1.9  
[Clicknium Python Module](https://pypi.org/project/clicknium/) >= 0.1.10

### Install from Clicknium Python Command
```Python
from clicknium import clicknium as cc

# install chrome extension
cc.chrome.extension.install()

# install edge extension
cc.edge.extension.install()
```

### Install from Clicknium Visual Studio Code Extension
Find the `AUTOMATION TOOLS` tab in the `Clicknium Extension Panel` and click the `Install` button.

![automation tools](./img/automation_tools_tab.png)
