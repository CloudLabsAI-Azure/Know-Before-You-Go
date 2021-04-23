# Analytics in a Day

## Known Issues and workarounds 

1. The dedicated SQL pool is paused by default, the attendee must resume the pool before performing the lab by following the below steps.

    - Navigateto the **Synapse-AIAD-287302** resource group from the Azure portal.
    
    - Select dedicated SQL pool **SQLPool01 (asaworkspaceUniqueID/SQLPool01)** and click on **Resume**. 
    
    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/sparkpool.png?raw=true)

1. If attendee face issues while trying to access the environment, follow the below steps:

    - They can check to see if the VM is in the running state, if not they can start it from the Virtual machine tab. 
  
    - It could also be due to a duplicate window open in another browser, we suggest closing all windows and trying again. Or using a private window and clearing the cookies.  

1. Issue with Spark pool:

	**Failed to start the Spark Session error**
	
	Solution: **Refresh** the browser tab
	
      - There might be multiple notebooks open because of which this issue occurs usually ,Refresh will work and also users can cancel any existing spark applications if they are still running under Monitor section.
      
      - Eventhough notebooks are not open, sometimes attendee might receive this error. Attendee can refresh and try to perform that step again.
      
1. If **SQL Built in/on demand** is **Unreachable/Offline**, then

     - Your network prevents communication to Azure Synapse backend. Most frequent case is that port 1443 is blocked. To get the builtin to work, unblock this port. Other problems could prevent builtin to work as well. Attendee can follow the below link to troubleshoot the issue.
     
        https://docs.microsoft.com/en-us/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio

1. Sometimes core capacity of the **spark pool** can exceed, attendee can refresh the browser/stop the session then restart it and try to access again. 

1. If the attendee is not able to find the options **Connect to** to attach spark pool and **Language** that is to be used, attendee can follow any on the listed solutions to reslove the issue.

      1. Attendee needs to reset the zoom level accordingly so that he will be able to see the options and provide values accordingly.
      1. Attendee can click on more button (**...**), then he will be able to see the options and provide values accordingly.
      
           ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-integratedenv.png?raw=true "Linked service")

      
1. Exercise 2 Task 2 : **Enrich Customer Data** data flow execution failure.

    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-coreissue.png?raw=true)

    - If **Enrich Customer Data** data flow execution fails due to vcore quota issue, attendee can rerun the data flow execution as it is a temporary issue.
    
1. Exercise 3 Task 2 - Create a Power BI report in Synapse  

   If attendee is not able to see a list of data fields under Fields, follow the steps 1-14 given in the lab guide after step 2.

1. Exercise 3: Power BI integration 

     Sometimes the PowerBI licence does not get assigned automatically and attendee will be unable to find the PowerBI option under Develop hub in Synapse Analytics Workspace.
     
      ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-powerbi-7.png?raw=true "Linked service")
     
     Attendee can follow the below steps to trobuleshoot the issue by create a new Power BI workpace and linked service:
     
     1. Navigate to PowerBI Portal  www.powerbi.com 
     
     2. Sign in using the Azure Credentials, you can find the Credentials from the **Environment Details** tab.
     
          ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-powerbi-1.png?raw=true "Linked service")
              
     3. From the left-hand side menu, select **Workspaces** then click on **Create a workspace**.
     
         ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-powerbi-2.png?raw=true "Linked service")
     
     4. Provide worskpace name as **PowerBIWorkspace{Uniqueid}** and click on **Save**. You can find the **Uniqueid** from the **Environment Details** tab.
     
         ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-powerbi-3.png?raw=true "Linked service")
         
     5. Launch Synapse studio, select **Manage** from the left-hand side menu and click on **Linked services**.
     
         ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-powerbi-4.png?raw=true "Linked service")
              
     6. Click on **+New**, serach for and slect **PowerBI** then click on **Continue**.
     
         ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-powerbi-5.png?raw=true "Linked service")
              
     7. On the **New linked service (Power BI)** blade, provide the following values and click on **Create**.
     
           - Name : **PowerBIWorkspace**
           - Tenant: select the tenant from the dropdown.
           - Worskpace name : select the workspace **PowerBIWorkspace{Uniqueid}** from the dropdown.

         ![Linked service](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-powerbi-6.png?raw=true "Linked service")
	 
     8. Once created, click on **PublishAll** then **publish**.
         
1. Exercise 3: Power BI integration 

    - Power BI desktop is already downloaded and installed in the virtual machine provided with the lab; the attendees do not have to download it again.

1. Attendee will not be able to perform **Exercise 5 - Data Science with Azure Synapse Spark** as it is **Read-Only** exercise.

      - Exercise 5 is currently Read only/Optional. Attendes can just go through it but will not be able to perform the steps as part of the lab.

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

1. Exercise 4  Task 1  Step 8 : **For the Legend (series) column, select CustomerKey**

      - Synapse workspace dashboard gets blank, If you get this issue please reach out to [CloudLabs-support](cloudlabs-support@spektrasystems.com)

	![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-Environment9.png)
