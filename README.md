# Assignment 1 - Scan and read outlook email content


At the end of this exercise we want to achieve the following result:
![Project test result](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Test_Result.png)

## SAP iRPA Desktop Studio

#### Step 1: Start new project
Start a new project by going to File > New Project. Now enter details and press Save.

![Start new project](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Start_New_Project.png)

#### Step 2: Add outlook library
If you want to use outlook in your project, you need to add the outlook specific library. Do this by going to File > Edit Project > Libraries tab and selecting it from the list.

![Add outlook library](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Add_Outlook_Library.png)

#### Step 3: Add new workflow
An iRPA project always needs a workflow to function. The workflow contains the steps that need to be executed by the Desktop Agent. Go to the Workflow tab and right click on the left part of the screen. Select New Workflow, fill details and press Save.

![Add new workflow](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_New_Workflow.png)

#### Step 4: Add popup to workflow
In this assignment we want to show a popup to the user with the content of a specific email. The workflow needs to trigger this popup. In the right bottom part of the screen, select the Activities tab and search for msgbox. Now drag the msgbox element to the workflow canvas and drop it on the down facing arrow coming from the Start element.

![Add popup](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Add_Popup.png)

#### Step 5: Popup details & build project
Select the msgbox element you just created. Now in the upper right part of the screen, fill some details regarding the popup element. Next, press the Build button in the icon bar. This will generate the scripts for all the objects in the project.

![Build project](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Popup_Details_and_Build.png)

#### Step 6: Edit popup script
Go to the Scripts tab. If the build was succesful, an entry should be visible for the workflow you have created. Double click the entry for your worflow. This will open the scripts related to it. For this assignment, it means there was a script generated to display the msgbox.

We will abuse the popup script to add additional logic. Add the code below to the script on the highlighted position and save it.

![Edit script](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Edit_Script.png)

```javascript
	// Scan and Read Email
  var mails = [];
  var i = 0;
	var message = "";
	var mailBody = "";
	
	ctx.log("Start Email Scan");
	
  ctx.outlook.init();
  ctx.outlook.mail.resetMailCollection();
  ctx.outlook.mail.searchByCriteria( { subject: "testing123", dontThrowExceptionIfNoMailFound: true });
	mails = ctx.outlook.mail.getFilteredTable();
	if (mails.length) {
		ctx.each(mails,function(index,mail) {
			
			// Retrieve email
			ctx.outlook.mail.retrieveMail( {
				EntryID : mail.EntryID, 
				StoreID : mail.StoreID
			});
			
			// Fetch and log email body
			mailBody = ctx.outlook.mail.getBody(index);
			ctx.log(mailBody);
			
		});
		
		message = mailBody;
		
		// If email was read & processed, I want to move it to a specific folder, but thats not working :( 
		//ctx.outlook.mail.moveToSpecificStore(0, 'iemke.kooijman@innov8ion.nl', 'Inbox\\test');
		
	} else {
		message = 'Mail not found :('; 
	}
	ctx.outlook.end();
	ctx.log("End Email Scan");
```

#### Step 7: Run & test project
Now everything is in place to run a test. Press Debug button on the icon bar. This will open & load the project in the Desktop Debugger. Wait untill the project is running. Now go to your windows taskbar and click the Desktop Agent icon. Click your workflow name in the list. This will run the project. 

![Run and test](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/blob/master/img/1_Run_and_Test_Project.png)

#### Step 8: Open the log that was generated for the run
