# Azure Immersion Workshop: Data Modernization

Instructor should make sure that the attendees follow the **lab guide** provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guide and MCW repo lab guide. 

### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Know issues in Lab Steps

1. #### IMPORTANT!! 

   - Whenever attendee is asked to provide value for SUFFIX, it should be replaced with value which can be found from the Environment Details page.
   - Not providing the SUFFIX value will lead to 
   
        - **Deployment issues** while deploying new resources, 
           
        - **Connection issues:** while connecting to database using **Microsoft SQL Server Management Studio 17(SSMS)** and** while performing **Database Assessment and Database Migration**. 



1. #### Exercise2 Task4 Step5:

   - While creating the storage account, make sure attendee provide the values as follows: 

       - Resource group: select existing then provide name hands-on-lab-SUFFIX 
       - Storage account: select Create new then provide name as **shellstorageSUFFIX** 
       - file share: select Create new then provide name as **shellfileSUFFIX** then create storage 

   - Attendees can find the SUFFIX value from the Environment Details page. 

    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/suffix.png?raw=true)

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


1. #### Exercise1 Task1 Step3: Not able to see the Add Vnet buttom from VM.

   We are having a temporary issues related with Azure UI, This may be removed in furture once the issue is fixed. 
   
   1. On Exercise1 Task1 Step3 if you cant able to see the Vnet button then please login to Azure Portal from your local Machine and follow the Vnet integration task, Once the task is done you can switch back to the VM. 

      ![image](https://user-images.githubusercontent.com/45102602/128701347-8f786a12-0944-4e1e-9d09-b3fe5c1117e0.png)


