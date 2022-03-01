# Azure Immersion Workshop: Infrastructure Migration

Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/4c14777d-6338-4016-9ac6-ba7b050a4816)

## Known issues and workarounds

- [Known issues in Lab Steps](#Known-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

## Known issues in Lab Steps 

### 1. **Exercise1 -> Task3 -> Step3**: 

   If attendee receive a prompt asking for credentials after launching the **Azure Migrate appliance configuration wizard** using the shortcut available on the desktop, follow the below instructions:
   
   1. From the Azure Migrate Appliance VM, open IIS manager and select the **Conections** that starts with **WIN**.

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/lob-issue-03.png?raw=true)
      
   1. Now, select **Authentication** under IIS from the home page.

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/lob-issue-04.png?raw=true)
      
   1. Select **Windows Authentication** and click on **Enable** to enable it.

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/lob-issue-05.png?raw=true)
   
   1. Close the **Azure Migrate appliance configuration wizard** and re-launch it using the desktop shortcut.

### 2. **Exercise1 -> Task3 -> Step17**: 
    
If attendee see that the discovery process is stuck at **Discovery is in progress** state for more then 5 mintues, then please follow the below steps for workaround.
    
![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/progress.png?raw=true)
   
   ### Workaround 1:
   
   1. Open HyperV Manger and do right click on the **AzureMigrateAppliance** server and select **Turn off** button. 

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/hypervshut.png?raw=true)
      
   1. After a few seconds double click on the **AzureMigrateAppliance** Server and a popup will show then click on **Start** button to start the HyperV server. Enter **demo!pass123** Password on login screen.
    
        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/start.png?raw=true)
     
   3. Once the HyperVM is up please switch back to azure portal in the labvm and click on refresh button to get the latest information. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/refresh.png?raw=true)
     
   4. Now you should be able to see that is discovery progress is completed. as shown in the below screenshot.

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/done.png?raw=true)

   ### Workaround 2: 
   
   If you still see that the discover items is not visible then you can follow the below steps. However servers are discovered already but due to a Azure GUI issue its not visible on this page.

   1. Go to the **Azure Migrate** blade in the Azure portal.  Select **Windows, Linux and SQL Server**, and then click on **Appliance** button.
      ![Screenshot of the Azure Migrate appliance configuration wizard, showing the 'Appliances' button.](https://raw.githubusercontent.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/snapshot/Hands-on%20lab/images/Exercise1/Discovered_Servers_Count.png "Appliances")
      
   2. On the **Appliance page**, Go to the Overview, you should see a count of the number of servers discovered so far.
      
      ![Screenshot of the Azure Migrate portal blade. Under 'Azure Migrate: Server Assessment' the value for 'Machines' is '5'.](https://raw.githubusercontent.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/snapshot/Hands-on%20lab/images/Exercise1/Machines.png "Machines")
    
   3. If you are able to see the number of server then you can continue the lab from Exercise 1 Task4. 
     
### 3. **Exercise2 -> Task3 -> Step16**:    

If attendee gets below error while connecting to the target SQL database in the process of migrate project creation, you can delete the existing **SmartHotel-DB-for-DMS** endpoint, recreate it and then perform Task3 again.
    
![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/Lob-dms-issue.png?raw=true)


### 4. **Exercise1 -> Task6 -> Step1**: 

   If attendees notice that the dependency agent status is showing as **Requires Agent Installation** instead of Installed even after installing dependency agents in all the three VMs, This is because there is an ongoing issue from Azure end where the latest status is not getting reflected in dependencies blade. Please follow the steps below to confirm dependency agent installation in VMs using **Log Analytics workspace**.
   
   1. Search for **AzureMigrateWS** Log Analytics workspace under **Azure Migrate** RG.

      ![Screenshot showing the view dependencies button in the Azure Migrate VM group blade.](https://github.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/blob/prod/Hands-on%20lab/images/Exercise1/dependency-1.png?raw=true "View dependencies")


   1. Select **Logs (1)** under General category, enter the below query and click on **Run** **(2)** to review the connected servers information.

       ```
       Heartbeat
       ```

      ![Screenshot showing the view dependencies button in the Azure Migrate VM group blade.](https://github.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/blob/prod/Hands-on%20lab/images/Exercise1/dependency-2.png?raw=true "View dependencies")



      ![Screenshot showing the view dependencies button in the Azure Migrate VM group blade.](https://github.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/blob/prod/Hands-on%20lab/images/Exercise1/dependency-2.1.png?raw=true "View dependencies")
     
   1. Notice the **SmartHotelWeb1**, **SmartHotelWeb2** and **UbuntuWAF** servers have the required agents intsalled and are connected to the workspace.
       ![Screenshot showing the view dependencies button in the Azure Migrate VM group blade.](https://github.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/blob/prod/Hands-on%20lab/images/Exercise1/dependency-3.png?raw=true "View dependencies")
      
### 5. **Azure API issue**: 

- Due to recent changes in Azure API's, Azure API's are taking some additional time to fetch the details of the resources. The validation steps for the lab may fail at first, but if you re-run them after 30-45 minutes, they will get succeed if there are no configuration related issues with the lab steps you performed.
