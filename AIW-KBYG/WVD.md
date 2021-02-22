# Known Issues and workarounds 


1. The attendees may face issues while trying to access the environment, 
    - they can check to see if the VM is in the running state, if not they can start it from the Virtual machine tab. 
    - It could also be due to a duplicate window open in another browser, we suggest closing all windows and trying again. Or using a private window and clearing the cookies.  

1. Exercise 1 Task 2  Step 4 

   A. Project Details     

   **Location** – make sure this is the same as the region of the resource group to avoid any errors. 
   
1. Exercise 1 Task 2  Step 4 
   
   - In case Host Pool deployment fails, follow the below steps. 

     1. Go to the WVD-RG resource group and click on Overview.

       ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/wvd-issue1.png?raw=true)

     1. Select the resources highlighted in the image below, then click on ellipsis in the top-right corner and click on delete. Make sure you DO NOT delete any other resources other than the ones shown in screenshot below.
     
       ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/wvd-issue2.png?raw=true)

     1. Now under Confirm delete type yes in the bar and click on Delete.

       ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/wvd-issue3.png?raw=true)

     1. Once the resources get deleted, then perform Task 1 from Step 1 to Step 11 to create the Host Pool again.

     1. Now wait for the deployment to succeed. When it gets succeeded, open the notifications and click on Go to Resource.

       ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/wvd-issue4.png?raw=true)

1. Exercise 3 Task 1 Step 6 

   - The user might get an error while signing into office, as the account cannot be used to activate office in a shared computer scenario. We can ignore this and proceed with the lab.  

1. Exercise 4 Task 1 Step 13 

   - The user might get an error while signing into office, as the account cannot be used to activate office in a shared computer scenario. We can ignore this and proceed with the lab.  

1. Exercise 4 Task 2 Step 2 

   - While creating the storage account, make sure attendee provide the values as follows: 

       - Resource group: select existing then provide name WVD-RG 

       - Storage account: select Create new then provide name as sa{UniqueID} 

       - file share: select Create new then provide name as fs{UniqueID} then create storage 

       - Attendees can find the UniqueID value from the environment details page.  

1. Exercise 5 Task 2 Step 2 

   - If attendee is not able to add the role assignment to file share: 

   - Attendee should make sure that step 7 of task 1 of exercise 5 has been performed. 

       - “In the storage account, click on Configuration present under Settings blade. Then scroll down and find the option Active Directory Domain Services (Azure AD DS). Select Enabled for it.” 

1. Exercise 5 Task 2 : Validation Failure 

   - If the validation fails, attendees should make sure that Storage File Data SMB Share Contributor role is assigned to the file share userprofile which is created as a part of the lab. 

1. Exercise 6 Task 3 : Validation Failure 

   - If the validation fails attendee should make sure that all the configurations provided in the lab guide are followed while adding the **ApplicationGroupMonitoring** Diagnostic setting. 
