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


In Visual Studio Code, press "Ctrl+Shift+P" to show the Command Palette, and enter "Clicknium" to select and show "Create Clicknium Project". Press "Enter", and select the folder where the project is stored according to the pop-up window. 
![project create](../img/project_create.gif)

When the project is created, a pop-up window in the lower right corner shows the general restored project information and the bottom page shows details. After restoring, the current Python virtual enviroment can be seen when you open app.py.
![project create](../img/create_project_apppy_env.png)

**项目结构**
![project structure](../img/create_project_1.png)

In Visual Studio Code, press "Ctrl+Shift+P" to show the Command Palette, and enter "Clicknium" to select and show " Run". When you press "Enter" to run the project, Clicknium extension will deploy the project running process based on app.yaml.

1. **app.py** an automation scripts file where the main function is the entry function for runing the project.
   ![project appyy](../img/create_project_apppy.png)
2. **app.yaml** configuration files where you can configure the project, Python version, Python package, project entry file, cloud element repository, etc.
   ![project appyaml](../img/create_project_appyaml.png)
   - startUp: The project entry file, if you want to change the project run entry file to main.py, fill out "main" to configure it.
   - Log：The project log, currently supporting the local log where "Folder" indicates the path of the Log storage Folder. If this parameter is  blank or null, it will be automatically stored in the Log file starting with %LOCALAPPDATA%\Clicknium\Log\Folder Automation.
   - requirements：running project dependency
     &emsp;Python:Python version is 3.7.0 by default.In the creating a project, Clicknium extension automatically reads the current Default Interpreter Path Settings in Python Settings in Visual Studio Code. If this setting uses neither Python virtual environment path nor the Python embedded version path, Clicknium extension read this setting to change the Python version to the configuration. 

     ![project appyaml](../img/create_project_appyaml_python_config.png)
     &emsp;Packages：Python package dependency. In this configuration, you can add one or more Python packages requrired in projects in the format of package-version. If the version is blank or null, the latest version will be used automatically.
     ![project appyamlpython](../img/create_project_appyaml_python.png)
     If there is no need for  Python package dependency，it will be configured as [].
     ![project appyamlpython](../img/create_project_appyaml_python_clear.png)
     &emsp;locators: The cloud element repository dependency, configured in the same way as Python package dependency.
3. **logo.ico**：Generate the file with exe icon when packaging the project, and it can be replaced with the needed icon file.
4. **.gitignore**：When using Git, you can add or remove files that you want to ignore.

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

- Run the project

  In Visual Studio Code, press "Ctrl+Shift+P" to show the Command Palette, and enter "Clicknium" to select and show " Run". When you press "Enter" to run the project, Clicknium extension will deploy the project running process based on app.yaml
  ![project run](../img/run_project.gif)
- Debug the project
  **Basics**
  
  In Visual Studio Code, set a breakpoint on the right side of the code editing window at first,
  press "Ctrl+Shift+P" to show the Command Palette, and enter "Clicknium" to select and show " Debug". When you press "Enter" to run the project, Visual Studio Code will be debuging with the debug button shown at the top. 
  ![project debug](../img/debug_project_3.png)
  &emsp;Continue (F5) / Pause (F6)
  &emsp;Step over (F10)
  &emsp;Step in (F11)
  &emsp;Step out (Shift + F11)
  &emsp;Restart (Ctrl+Shift+F5)
  &emsp;Stop (Shift + F5)
  ![project debug](../img/debug_project.gif)
  **Monitor Variables**In the upper left corner of Visual Studio Code, you can see the variables is debugging the running values.
  ![project debug](../img/debug_project_1.png)
  **Debug Console**In Visual Studio Code, open the debug console by "View -> Debug Console" 
  ![project debug console](../img/debug_project_2.png)

## For Existing Project
