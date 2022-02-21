# Known Issues and workarounds 

- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

 1. **Azure API issue**: 

     - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.

1. The attendees may face issues while trying to access the environment, 
    - they can check to see if the VM is in the running state, if not they can start it from the Virtual machine tab. 
    - It could also be due to a duplicate window open in another browser, we suggest closing all windows and trying again. Or using a private window and clearing the cookies.  

1. **Lab 1 Exercise 1 Step 3**: 

   A. Project Details     

   **Location** – make sure this is the same as the region of the resource group to avoid any errors. 
   
1. **Lab 2(A)**:

   - After completing Lab 2(A), The data in Azure Insights won't be loaded immeditately. It might take some time to load the data. Please perform the Lab 2(B) at the last and check the data.

1. **Lab 3 Exercise 1**:
  
   - Attendee should perform this exercise in their Own **PC/computer/workstation** not in the **JumpVM**. Peforming this exercise in **JumpVM** will cause connection issues when try to access the the published applications using WVD Desktop Client. 

3. **Lab 3 Exercise 1 Step 13**: 

   - The attendee might get an error while signing into office, as the account cannot be used to activate office in a shared computer scenario. We can ignore this and proceed with the lab.  

1. **Lab 6 Exercise 2 Step 9**: 

   - If attendee is not able to add the role assignment to file share then: 

     - Attendee should make sure that step 7 of task 1 of exercise 5 has been performed. 

        - “In the storage account, click on Configuration present under Settings blade. Then scroll down and find the option Active Directory Domain Services (Azure AD DS). Select Enabled for it.” 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/wvd-issue6.png?raw=true)

1. **Lab 6 Exercise 2 : Validation Failure** 

   - If the validation fails, attendees should make sure that Storage File Data SMB Share Contributor role is assigned to the file share userprofile which is created as a part of the lab. 
