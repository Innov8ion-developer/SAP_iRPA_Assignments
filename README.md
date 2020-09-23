# Assignments for the Innov8ion night about SAP iRPA
This repository is created to host a number of assignment for the Innov8ion night about SAP iRPA.

#### Prerequisites
Before starting these assignment, make sure you have completed prerequisite installations, account creation and account setup. All prerequisites can be found in the following blog:
https://blogs.sap.com/2019/12/26/sap-intelligent-rpa-trial-get-ready-to-build-bots.../

#### Use case
A team is responsible for creating new suppliers in the SAP system. The team receives emails with information about new suppliers on a daily basis. Before entering this data in the SAP system, a team member looks up additional information regarding the supplier on the dutch KVK website. Once he has collected all the data he needs, he heads over to the SAP Fiori Launchpad to submit a new supplier in the Supplier Master Fiori app.

To save costs, free up time for more important tasks and reduce data input errors by employees, this process will be automated using SAP iRPA. A bot will be build to handle three key components:

1. Scan an outlook e-mail inbox for emails with a specific subject. If an e-mail was found, extract all supplier data from it
2. Read additional data for this supplier using the KVK API
3. Enter all information in the Supplier Master Fiori app and create the new supplier in the SAP system

#### Assignments
This repository has a few branches. Every branch is an assignment you can do seperately. However, the best idea would be to combine the assignments to create a complete flow of the components above. This means you have to tweak the assignments to make them flow into eachother smoothly.

[Go to Assignment 1](https://github.com/Innov8ion-developer/SAP_iRPA_Assignments/tree/1_Scan_and_Read_Email/README.md)
