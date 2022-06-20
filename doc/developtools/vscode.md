# Clicknium VSCode Extension<!-- {docsify-ignore-all} -->

  - [Overview](#overview)
  - [Create Project](#create-project)
  - [Extension Installation](#extension-installation)
  - [Record UI Locators](#record-ui-locators)
  - [Edit and Validate Locator](#edit-and-validate-locator)
  - [Writing code](#writing-code)
  - [Run/Debug Project](#rundebug-project)
  - [For Existing Project](#for-existing-project)

## Overview
For python developers, ClickCorp provides clicknium extension that include all RPA features. 
 You can create python automation project, capture UI elements in browsers and in various desktop applications, easily edit UI locator, validate or recapture, run/debug the automation project, and provide centeral locator store management on the cloud.
 Besides, Clicknium also improves writing code experience, such as providing IntelliSense, error hint, etc.

***Installation​***: Install through VS marketplace `Clicknium VS Code extension` or search clicknium in Visual Studio Code.  
***Remarks***: As Clicknium extension is completely free, developers can use all features in Visual Studio Code.

## Create Project

在 Visual Studio Code 中，按下"Ctrl+Shift+P"组合键以显示"命令面板"，然后键入"clicknium"以筛选并显示"Create Clicknium Project"命令。按"Enter"，根据弹窗选择项目存储的文件夹即可
![project create](../img/project_create.gif)
项目创建后，在 Visual Studio Code 的右下角以及下方 Output 会有提示，可以看到项目还原信息，还原完成后，打开 app.py 将会看到当前使用 python 环境信息
![project create](../img/create_project_apppy_env.png)

**项目结构**
![project structure](../img/create_project_1.png)
在 Visual Studio Code 中，当用于按下"Ctrl+Shift+P"组合键以显示“命令面板”，然后键入"clicknium"以筛选并显示"Run"命令,按"Enter"来运行项目时,Clicknium 扩展将会根据 app.yaml 配置来运行项目流程；

1. **app.py**为脚本文件，用于您编写自动化脚本，其中 main 函数为项目运行入口函数。
   ![project appyy](../img/create_project_apppy.png)
2. **app.yaml**为配置文件，用于您配置项目，Python 版本，Python 包，项目入口文件，云端元素库等信息，
   ![project appyaml](../img/create_project_appyaml.png)
   - startUp:项目入口文件，如果您想项目运行入口文件改成 main.py，在此配置只需要填写 main 即可；
   - Log：项目日志，目前支持本地日志记录，其中 Folder 表示存储日志存储文件夹路径，若不填写或者 null 的时候，将自动存储在%LOCALAPPDATA%\Clicknium\Log\文件夹 Automation 开头日志文件中；
   - requirements：项目运行依赖
     &emsp;Python:Python 版本，默认 3.7.0，在项目创建中 Clicknium 扩展会自动读取您当前 Visual Studio Code 中关于 Python 设置中 Default Interpreter Path 设置，如果该设置使用不是 Python 虚拟环境路径或者 Python 嵌入式版本路径，Clicknium 扩展将采用该设置并将读取 Python 版本修改到配置；
     ![project appyaml](../img/create_project_appyaml_python_config.png)
     &emsp;Packages：Python 包依赖，在此配置可以添加一个或者多个项目中需要用的 Python 包，格式 package-version，其中 version 若不填写或者为 null 将自动使用最新版本；
     ![project appyamlpython](../img/create_project_appyaml_python.png)
     若不需要任何 Python 包依赖，将此处配置成[]即可
     ![project appyamlpython](../img/create_project_appyaml_python_clear.png)
     &emsp;locators:云端元素库依赖，配置方式和 Python 包依赖一致。
3. **logo.ico**：项目打包时生成 exe 文件图标文件，可以替换成需要 icon 文件；
4. **.gitignore**：当使用 git 版本管理的时候，可以添加或者删除需要忽略版本管理文件；

## Extension Installation
[Automation Extensions](./doc/developtools/extensions/extensions.md)

## Record UI Locators
In Visual Studio Code, press `CTRL+F10` to invoke Clicknium recorder and minimize current Visual Studio Code window.  
![clicknium recorder](../img/recorder_main.png)  
The capture technology indicates which automation technology currently used to capture UI elements. The supporting automation technology are as follows:
- UIA： Leverage Microsoft UI Automation, used for most windows application such as win32, winform, WPF application and so on
- IA: based on MSAA (Microsoft Active Accessibility)
- Java: automation for Java application, supporting JRE version above 1.6
- IE: automation for Internet Explorer, supporting version above 5.5 
- Chrome: automation for Chrome ,installation of chrome extension is need at first, supporting version above 60
- Edge: automation for Edge, installation of Edge extension is needed at first
- Firefox: automation for Firefox, installation of Firefox extension is needed at first, supporting version above 56
- SAP: automation for SAP WinGUI, SAP GUI Scripting setting is enabled at first 
  
Default is ***Auto Detect***, which means clicknium recorder automatically select the technology:  
If the mouse moves on Windows applicaiton, it will use UIA technology to locate the element;   
If the mouse moves on Java applicaiton, it will use Java technology to locate the element;   
If the mouse moves on Internet explorer, it will use IE technology to locate the element;   
If the mouse moves on Chrome, it will use Chrome technology to the locate element;   
If the mouse moves on Microsoft Edge, it will use Edge technology to locate the element;   
If themouse moves on Firefox, it will use Firefox technology to locate the element;   
If mouse moves on Sap windows GUI, it will use SAP technology to locate the element

Advanced Option: default is None, when you choose `XPath`, it will immediately affect on web automation technology (IE, Chrome, Edge, Firefox) while capturing the element, and generate locator in XPath style.

Cursor Position(X,Y): current mouse postion on the screen

After invoking Clicknium Recorder, it will highlight the element recognized by moving the mouse to the target application. 
If you want to capture the element, press `Ctrl` and click to add  the element locator.

![clicknium recorder](../img/record1.gif) 

## Edit and Validate Locator
After recording the locators, you can open and edit the locator. 
![clicknium vscode](../img/main.png) 

- locator store: the file to store locator data. The locators of the same application are stored in one locator store by default. Users can manage the locator store in Visual Studio Code or Clicnium Recorder.
- locator: UI element locator, the string(XML fragment) that used to find the element including application information and all necessary parent nodes of the UI element, and  attributes of each element itself.
- Screenshot: While recording the elements, store the screenshot together with the locator
- Attributes: Users can select/deselect or edit the value of each attribute.

More about the locator, please refer to [clicknium locator](./doc/automation/locator.md)

After editing the locator, you can press button`Validate`, it will minimize Visual Studio Code and highlight the found element. If not found, it will show detailed errors.
![validate error](../img/validate_err.png)

## Writing code
- Auto Code Complete
Set the locator as the parameter, for example, `cc.find_element(`, you can press `Ctrl`+F10 to invoke Clicknium Recorder and capture the elements. Return to Visual Studio Code, the captured element will be automatically filled like `cc.find_element(locator.chrome.bing.search_sb_form_q)`

- IntelliSense
If you want to choose one locator in the locator store, Clicknium code extension can show you the locator store list and the locator list.  
![intellisense](../img/intelliSense.png)
## Run/Debug Project

- 运行
  在 Visual Studio Code 中，按下"Ctrl+Shift+P"组合键以显示“命令面板”，然后键入"clicknium"以筛选并显示"Run"命令,按"Enter"来运行项目时,Clicknium 扩展将会根据 app.yaml 配置来运行项目流程；
  ![project run](../img/run_project.gif)
- 调试
  **基本**
  在 Visual Studio Code 中，先在代码编辑窗口右侧设置断点，按下"Ctrl+Shift+P"组合键以显示“命令面板”，然后键入"clicknium"以筛选并显示"Debug"命令,按下"Enter"，Visual Studio Code 将处于调试状态，并且在顶部出现调试按钮
  ![project debug](../img/debug_project_3.png)
  &emsp;继续(F5) / Pause 暂停(F6)
  &emsp;单步跳过 (F10)
  &emsp;单步调试 (F11)
  &emsp;单步跳出 (Shift + F11)
  &emsp;重启 (Ctrl+Shift+F5)
  &emsp;停止 (Shift + F5)
  ![project debug](../img/debug_project.gif)
  **监视变量**在 Visual Studio Code 中左上角，可以看到变量在调式运行的值
  ![project debug](../img/debug_project_1.png)
  **调试控制台**在 Visual Studio Code 中，打开调试控制台的方式为"查看->调试控制台"
  ![project debug console](../img/debug_project_2.png)

## For Existing Project
