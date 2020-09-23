# Assignment 3 - Create supplier in Supplier Master Fiori app
In this assignment you are going to create an SAP iRPA project that starts the Supplier Master Fiori app and navigate through it to create a new supplier. The data that was collected in the earlier assignments then gets entered in the corresponding fields. A new supplier can then be saved.

At the end of this exercise we want to achieve the following result:
![Project test result]()

## SAP iRPA Desktop Studio

#### Step 1: Start new project
Start a new iRPA project similar to assignment #1

#### Step 2: Add new application & page
In this assignment we are going to control the pages of an application. The application in this assignment is the SAP Fiori Launchpad. To start using it, we need to capture it and add it to the project. 

First, make sure you have the SAP Fiori Launchpad open and logged in. In the Applications tab, press Add Application. If you press the refresh button in the popup window, you should be able to see the browser as an application with the SAP Fiori Launchpad in it. Select it and press Save and Capture Page. We have now captured the browser as an application. Directly after, repeat the process to add the the SAP Fiori Launchpad as a page.

#### Step 4: Add recognition criteria & select tile element
Everything that gets captured in your project needs to be uniquely identified by a recognition criteria. To do this, select the application you have just added in the list on the left side of the screen. Now take a look at the bottom part of the screen. Here you will find a Captured Data window and a Criteria window. You need to select a parameter from the Captured Data window to uniquely identify the application. In this case we can click on the URL parameter to be our criteria. Repeat the process for the page you have added.

#### Step 5: Add the tile element
If you want to interact with something on the page you have just added, it also needs to be selected and identified. On the Fiori Launchpad, we want to start the Supplier Master Fiori app. Look for it on the canvas area and click it. It will then be highlighted. Now right click on it and select Associate to New Item. It will now be listed right underneath your application and page. For this element, also select a recognition criteria and save your project.

#### Step 5: Add new workflow
Add a new workflow similar to assignment #1

#### Step 6: Add page to workflow
In the Workflow tab, on the bottom right part of the screen is the Activities window. In it, select the Pages tab. You will find the application that you have added earlier here. Press the arrow button, now the page wil also be visible. Drag it onto the Workflow canvas and drop it on the down facing arrow from the Start element.

#### Step 7: Add a click activity
Double click the page you have just dropped onto the Workflow canvas. Look for the tile element you have identified. Now find the Click activity in the Activities window and drag it onto the tile element. Save the workflow.

#### Step 8: Run & Test project
Now everything is in place to run a test. Press the Debug button on the icon bar. This will open & load the project in the Desktop Debugger. Wait untill the project is running. Now go to your windows taskbar and click the Desktop Agent icon. Click your workflow name in the list. This will run the project. The SAP Fiori Launchpad should appear and the Supplier Master app should be started.

#### Step 9: Add Supplier Master page
Make sure the Supplier Master app is opened. Go back to the Applications tab and right click your application. Select Capture a New Page. Press refresh and now select the Supplier Master app. Save it.

#### Step 10: Add the create button element
Because we want to interact with the create button, also add this in the same way as you did in step 5.

#### Step 11: Add page to workflow
Add the additional page to the workflow in same way as you did in step 6.

#### Step 12: Add a click activity
Add the click activity to the create button in the same way as you did in step 7.

#### Step 13: Run & Test project
Now everything is in place to run a test. Press the Debug button on the icon bar. This will open & load the project in the Desktop Debugger. Wait untill the project is running. Now go to your windows taskbar and click the Desktop Agent icon. Click your workflow name in the list. This will run the project. The SAP Fiori Launchpad should appear and the Supplier Master app should be started and the create button should be pressed.

#### Next steps
The last step was not working for me. Can you make it work?

