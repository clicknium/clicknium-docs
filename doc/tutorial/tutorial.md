---
sidebar_position: 3
---

# Tutorial
This tutorial walks you through some of the fundamental Clicknium concepts, tools, and their usage while writing your [first automation code](./firstautomation.md).

# Installation
A Clicknium installation generally consists of the following components:
- [Clicknium Python Module](./../quickstart.md#install-clicknium-python-package): Clicknium automation core module, providing the API for UI automation.   
- [Clicknium VS Code Extension](./../quickstart.md#setup-clicknium-visual-studio-code-extension): Set up the development tool for coding automation script.
- [Clicknium Automation Extension](./../concepts/extensions/extensions.md): To get better performance, Clicknium provides some extension targeted to different environments and senarios. Developers can select the needed extension to install.  

Please follow [Quick Start](./../quickstart.md) to finish the installation.

# Clicknium Architecture Overview 
Clicknium is a platform where you can build your automation code. [Clicknium Python Module](./../quickstart.md#install-clicknium-python-package) provides programming interfaces to extract UI locators from **Locator Store** and automate UI elements in any application. The [Clicknium VSCode extension](./../concepts/vscode/vscode.md) provides Recorder to easily capture UI locators from any application and store them in Cloud/Local Locator Store. It also supports ***Code InteliSense*** to give a seamlessly coding experience and **Project** for better coding and execution management. The [Clicknium Cloud](../concepts/locatorstore.md#manage-cloud-locator-store) gives a chance to save and manage locators in the cloud and share locators cross projects/machines.  
![Clicknium Arc](./../img/Clicknium_arc.png)

# Clicknium Workflow
[Clicknium Recorder](./../concepts/recorder/recorder.md) can help you to capture UI element that you want to automate. After a successful capture, the recorder will generate a [Clicknium Locator](./../concepts/locator.md) target to the UI element and the locator will be send and store in [Clicknium Locator Store](./../concepts/locatorstore.md). You can create a [Clicknium Project](./../concepts/clickniumproject.md) to write your Python code. In the code, you can refer the locators stored in the Locator Store and operate via automation API provided by Clicknium Python Module.   
![automation flow](./../img/Clicknium%20tool.png)