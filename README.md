# Assignment 4 - Deploying to SAP Cloud Platform
In this assignment we are going to deploy the project that you have created to the SAP Cloud Platform iRPA environment. This will allow you to run the project through your own Desktop Agent.

## SAP iRPA Desktop Studio

#### Step 1: Create package
To package your project, press ALT+F5 of follow the path shown in the screenshot below. This will create a zip file in your project map.
![Create package](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/4_Create_Package.png)

## SAP Cloud Platform

#### Step 1: Log in to SAP Cloud Platform
Head over to the Cloud Foundry Environment. On the Subscriptions page, look for SAP Intelligent Robotic Process Automation and enter the application.

#### Step 2: Import package
Go to the Packages tab and choose to import a package. Go through the steps and select your zip file to import it. This will generate a Project in the Projects tab.
![Import package](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/4_Import_Package.png)

#### Step 3: Create environment
To run your project, we need to create an environment. Go to the Environments tab and click the New Environment button. Choose to create a DEV environment.
![Create environment](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/4_Create_Environment.png)

#### Step 4: Build up the environment
In your newly created environment, choose to add your package, add a trigger and an agent. For trigger type select Scheduled. Then select a timezone and select the entire block of time entries.
![Build environment](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/4_Build_Environment.png)

#### Step 5: Test project
To test out your project, go to the triggers tab and click the ... button. Click Run now. This will trigger your Desktop Agent to run the project.
![Test project](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/4_Test_Project.png)

#### End of assignments 
