# Azure Immersion Workshop: Data Modernization

Instructor should make sure that the attendees follow the **lab guide** provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guide and MCW repo lab guide.

Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/d0531fa5-76a1-4bdc-a477-466f34083856)

### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Known issues in Lab Steps

1. #### Exercise2 Task5 Step15:

   - If the status of **WwiMigration** activity appears as **Completed** then attendee can move on to the next task. Attendee can select **Refresh** every 5-10 seconds until the status is being changed to **Completed**.
  
   -  If the status of **WwiMigration** activity appears as **Log shipping in progress** then attendee can select **WideWorldImporters** under database name to verify the status for **WideWorldImporters.bak** and **WideWorldImportersLog.trn** files, if the status is **Restored** for both the files then attendee can move on to the next task. Attendee can select **Refresh** every 5-10 seconds until the status is being changed to **Restored**

     ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/datamod-issue.png?raw=true)

1. #### Exercise4 Task1 step4:

   - Here attendee needs to select available subnet for the app service, if the attendee is not able to select any subnet then attendee needs to follow the next instructions to create the subnet. while creating the subnet users' needs to make sure the subnet address space is not overlapping other subnet's address space 

1. #### Exercise2 Task5 Step5 :

   Cannot connect to your SQL VM while creating the migration project **OnPremToSqlMi**. Follow below instructions to resolve the issue.
      
    1. In Mssqlserver disable the VIA
    
    1. Turn off the firewall in the SQL vm, if we don't want to turn off the firewall we can create an inbound rule to allow 1433 port

1. #### Azure API issue: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.
