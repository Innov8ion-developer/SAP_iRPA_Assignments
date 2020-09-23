# Assignment 2 - Read additional data from KVK API
In this assignment you are going to create an SAP iRPA project that reads data from the KVK test API. The content from this API call will then be captured and displayed in a popup window.

We will use the url which calls the test version of the KVK API. This API does not require any authentication. You can test it directly in your browser by going to:
https://api.kvk.nl/api/v2/testsearch/companies?q=68727720

At the end of this exercise we want to achieve the following result:
![Project test result](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/2_Project_Result.png)

## SAP iRPA Desktop Studio

#### Step 1: Start new project
Start a new iRPA project similar to assignment #1

#### Step 2: Add new workflow
Add a new workflow similar to assignment #1

#### Step 3: Add Call webservice element to workflow
In this assignment we want to show a popup to the user with some content of the KVK test API call. The workflow needs to trigger the API call and the popup. In the right bottom part of the screen, select the Activities tab and search for web service. Now drag the Call web service element to the workflow canvas and drop it on the down facing arrow coming from the Start element.

In the Call web service element properties window, enter Source URL https://api.kvk.nl/api/v2/testsearch/companies?q=68727720 and an Input data variable.

![Add Call webservice element](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/2_Add_Call_Webservice_and_Details.png)

#### Step 4: Add Msgbox element to workflow & build project
Next we need to add the popup window. In the right bottom part of the screen, select the Activities tab and search for msgbox. Now drag the Msgbox element to the workflow canvas and drop it on the down facing arrow coming from the Call web service element.

In the Msgbox element properties window, enter Name, Title and Message properties.

Now press the Build icon in the icon bar. This will generate the scripts and objects needed for the project to run.

![Add Msgbox element](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/2_Add_Msgbox_and_Details.png)

#### Step 5: Edit scripts
The build may have caused some errors due to some incorrect variables. Fix the errors first before you continue.

Go to the Scripts tab. If the build was succesful, an entry should be visible for the workflow you have created. Double click the entry for your worflow. This will open the scripts related to it. For this assignment, it means there was a script generated to call the web service and display the msgbox.

We will adjust the web service script to store the received data in the GLOBAL variable and the popup script to display the stored data from the GLOBAL variable. Add the highlighted code below to the scripts and save it.

Also replace the fixed text from the popup with the newly introduced message variable.
![Edit scripts 1](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/2_Edit_Scripts_1.png)

![Edit scripts 2](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/2_Edit_scripts_2.png)

#### Step 6: Run & test project
Now everything is in place to run a test. Press the Debug button on the icon bar. This will open & load the project in the Desktop Debugger. Wait untill the project is running. Now go to your windows taskbar and click the Desktop Agent icon. Click your workflow name in the list. This will run the project. A popup should appear with the KVK details in it.

![Run & test project](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Run_and_Test_Project.png)

#### Step 7: Open the log that was generated for the run
Open the log that was generated for the run similar to assignment #1

[Go to Assignment 3](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/tree/3_Create_Supplier_in_Fiori_App/README.md)
