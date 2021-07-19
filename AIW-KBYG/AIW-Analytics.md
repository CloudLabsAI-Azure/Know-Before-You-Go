# Azure Immersion Workshop: Analytics

### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Know issues in Lab Steps 

1. The dedicated SQL pool is paused by default, the attendee must resume the pool before performing the lab by following the below steps.

    - Navigate to the **Synapse-AIAD-287302** resource group from the Azure portal.
    
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

1. Exercise 4  Task 1  Step 8 : **For the Legend (series) column, select CustomerKey**

      - Synapse workspace dashboard gets blank, If you get this issue please reach out to us via cloudlabs-support@spektrasystems.com

	![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/AIAD-Environment9.png)
