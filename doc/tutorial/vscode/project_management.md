---
sidebar_position: 3
---
# Project Management

## Overview
Clicknium project encapsulates Python automation files to guarantee the automation scripts having same result in developing, debugging, execution and distribution. 

## Create Project

In Visual Studio Code, press `Ctrl+Shift+P` to show the Command Palette, input or select `Clicknium: Create Project`, and then select a folder where the project is stored according to the pop-up window.
![project create](../../img/create_project.gif)

When the project is created, a pop-up window in the lower right corner shows the general project intialization information and the output panel shows details. After initialization, the current Python virtual enviroment can be seen when you open app.py.  
![project create](../../img/create_project_apppy_env.png)

## Run/Debug Project

### Run the project

In Visual Studio Code, press "Ctrl+Shift+P" to show the Command Palette, input or select "Clicknium: Run Project". The clicknium extension will deploy and run the project based on clicknium.yaml.
![project run](../../img/run_project.gif) 

### Debug the project

#### Basics

In Visual Studio Code, set a breakpoint to the code where you want to pause,
press `Ctrl+Shift+P` to show the Command Palette, input or select "Clicknium: Debug Project". The clicknium extension will start projec debugging with debug buttons shown at the top of Visual Studio Code.  
![project debug](../../img/debug_project_3.png)  
&emsp;Continue (F5) / Pause (F6)  
&emsp;Step over (F10)  
&emsp;Step in (F11)  
&emsp;Step out (Shift + F11)  
&emsp;Restart (Ctrl+Shift+F5)  
&emsp;Stop (Shift + F5)  
![project debug](../../img/debug_project.gif)

#### Monitor Variables

In the upper left corner of Visual Studio Code, you can see the variables is debugging the running values.  

![project debug](../../img/debug_project_1.png)

#### Debug Console

In Visual Studio Code, open the debug console by "View -> Debug Console"   

![project debug console](../../img/debug_project_2.png)


# Project Package

In Visual Studio Code, press `Ctrl+Shift+P` to show the Command Palette, input or select `Clicknium: Package Project`, then select the path to save the executable file.
![](../../img/pack_project.gif)

The detailed package log Output displays in the Output in Visual Studio Code.

Once the package is done, the saving folder will be opened to show the target executable file.

![pack project result](../../img/pack_project_result.png)

If you want to replace the Exe icon, replace the logo.ico file in the project file. 