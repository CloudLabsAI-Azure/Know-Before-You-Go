# MIGRATING SQL DATABASE TO AZURE

## Known Issues and workarounds

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

1. **Copy-Paste Issue**

    **If Copy paste doesn’t work, please try following:** 

      - Please check if Clipboard permissions are on **Allow**, if not then change it to **Allow**. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-1.png?raw=true) 

      - After allowing the clipboard content if you are not able to Copy the Content from lab Guide into the VM using copy button, then select the content which you want to copy from lab guide then right click > Copy to copy the content and then try to paste at desired location in Lab VM. 
      
      - Try to refresh the page or try any other Web Browser. 
      
      - Check on Network bandwidth in your local System/Laptop. 

     If the above points don’t work, then directly connect to the Lab VM using Remote Desktop Connection using the **Credentials** provided in **Environment Details** page.  

      - Copy the **LabVM/JumpVM DNS Name, Username** and **Password** from **Environment details** page 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-2.png?raw=true) 

      - Search for **Remote Desktop Connection** App from Start Menu items and then select the **Remote Desktop Connection** App. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-3.png?raw=true) 

      - Paste the **VM** **DNS Name** in Computer field and then, click on **Connect**. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-4.png?raw=true) 

      - Click on **More choices**. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-5.png?raw=true) 

      - Now, click on the **Use a different account.** 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-6.png?raw=true) 

      - Now, enter the **VM Admin username** and **password** which you have copied from Environment details page and click on **Ok** button. Please add dot and back-slash “**.\”** before the Admin username. 

         ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-7.png?raw=true) 

      - Next, click on the **Yes** button to accept the certificate and add in trusted certificates. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-8.png?raw=true) 

      - If **LabVM** opens on full screen, then you can **Restore Down** the window. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-9.png?raw=true) 

      - Split the Window from lab environment page to open the Lab guide in Separate Window. 

          ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-10.png?raw=true) 

      - Now, copy the lab environment URL from the list and open that inside the VM itself and then use the Vm on full screen. 

          ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-11.png?raw=true) 
