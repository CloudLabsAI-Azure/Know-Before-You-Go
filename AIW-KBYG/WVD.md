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

   - The attendee might get an error while signing into office, as the account cannot be used to activate office in a shared computer scenario. We can ignore this and proceed with the lab.  

1. Exercise 4 Task 1
  
   - Attendee should perform this exercise in their Own **PC/computer/workstation** not in the **JumpVM**. Peforming this exercise in **JumpVM** will cause connection issues when try to access the the published applications using WVD Desktop Client. 

3. Exercise 4 Task 1 Step 13 

   - The attendee might get an error while signing into office, as the account cannot be used to activate office in a shared computer scenario. We can ignore this and proceed with the lab.  

1. Exercise 7 Task 2 Step 2 

   - While creating the storage account, make sure attendee provide the values as follows: 

       - Resource group: select existing then provide name WVD-RG 

       - Storage account: select Create new then provide name as sa{UniqueID} 

       - file share: select Create new then provide name as fs{UniqueID} then create storage 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/wvd-issue5.png?raw=true)

       - Attendees can find the UniqueID value from the environment details page.  

1. Exercise 5 Task 2 Step 2 

   - If attendee is not able to add the role assignment to file share then: 

     - Attendee should make sure that step 7 of task 1 of exercise 5 has been performed. 

        - “In the storage account, click on Configuration present under Settings blade. Then scroll down and find the option Active Directory Domain Services (Azure AD DS). Select Enabled for it.” 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/wvd-issue6.png?raw=true)

1. Exercise 5 Task 2 : Validation Failure 

   - If the validation fails, attendees should make sure that Storage File Data SMB Share Contributor role is assigned to the file share userprofile which is created as a part of the lab. 

1. Exercise 6 Task 3 : Validation Failure 

   - If the validation fails attendee should make sure that all the configurations provided in the lab guide are followed while adding the **ApplicationGroupMonitoring** Diagnostic setting. 

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
