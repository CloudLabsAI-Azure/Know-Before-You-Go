# Azure Immersion Workshop: Infrastructure Migration

## Known issues and workarounds

- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Know issues in Lab Steps 

1. ### Important!! 


   - Wherever attendee is asked to provide value for **Location** same as your Azure SQL Database or same as your resource group, make sure to select the same region because selecting the different region will not allow the replication and migration of resources. 

1. **Exercise1 Task2 Step3**: 

   If attendee receives below error while generating the **Azure Migrate project key** in Azure Migrate. In this case go to the Azure Migrate main page and create a new project with different name, select that newly created project and perform the **Step 3 of Task2** again to generate the key.
   
   ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/LOB-issue.png?raw=true)
   
   **Note**: In this case, validations will fail, as the validation is configured to check the discovered servers, Assessments and AssessmentGroup under migrate project **SmartHotelMigrationDID** but attendee will be using different Migrate project in this case.
   

1. **Exercise1 Task3 Step17**: 
    
    If attendee see that the discovery process is stuck at **Discoery is in progress** state for more then 5 mintues, then please follow the below steps for workaround.
    
      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/progress.png?raw=true)
   
   ## Workaround 1:
   
    1. Open HyperV Manger and do right click on the **AzureMigrateAppliance** server and select **Turn off** button. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/hypervshut.png?raw=true)
      
    1. After a few seconds double click on the **AzureMigrateAppliance** Server and a popup will show then click on **Start** button to start the HyperV server. Enter **demo!pass123** Password on login screen.
    
        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/start.png?raw=true)
     
    3. Once the HyperVM is up please switch back to azure portal in the labvm and click on refresh button to get the latest information. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/refresh.png?raw=true)
     
    4. Now you should be able to see that is discovery progress is completed. as shown in the below screenshot.

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/done.png?raw=true)

   ## Workaround 2: 
   If you still see that the discover items is not visible then you can follow the below steps. However servers are discovered already but due to a Azure GUI issue its not visible on this page.

    1. Go to the **Azure Migrate** blade in the Azure portal.  Select **Windows, Linux and SQL Server**, and then click on **Appliance** button.
      ![Screenshot of the Azure Migrate appliance configuration wizard, showing the 'Appliances' button.](https://raw.githubusercontent.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/snapshot/Hands-on%20lab/images/Exercise1/Discovered_Servers_Count.png "Appliances")
      
    2. On the **Appliance page**, Go to the Overview, you should see a count of the number of servers discovered so far.
      
    ![Screenshot of the Azure Migrate portal blade. Under 'Azure Migrate: Server Assessment' the value for 'Machines' is '5'.](https://raw.githubusercontent.com/CloudLabs-MCW/MCW-Line-of-business-application-migration/snapshot/Hands-on%20lab/images/Exercise1/Machines.png "Machines")
    
    3. If you are able to see the number of server then you can continue the lab from Exercise 1 Task4. 
  

1. **Exercise1 Task6 Step1**:

     If you see that the Dependencies status as **Requires agent installation** instead of **Installed** in **Azure Migrate** even after installing the agents in the Virtual Machine, attendee can follow the instructions that are added to view service map from Log Analytics workspace in Exercise 1 Task 6 and they will be able to see the map. 
     
     ![lob2](https://user-images.githubusercontent.com/52440474/132685576-06b7e6a1-32be-472f-a0e6-f5fd64e9f57a.png)

     This is because there is an issue going on with Azure right now so that its not reflecting the latest status in dependencies blade. Attendee can review the service map from Log Analytics workspace and perform the next task as it will not affect the functionality of the lab.
         
1. **Exercise2 Task4 Step16**:    

    If attendee gets below error while connecting to the target SQL database in the process of migrate project creation, you can delete the existing **SmartHotel-DB-for-DMS** endpoint, recreate it and then perform Task4 again.
    
    
   ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/Lob-dms-issue.png?raw=true)
   
1. Issue while connecting to internet in **Azure Migrate Appliance vm**:

      1. Delete any extra switch if available.

      2. Re run below code and ensure DHCP server service is running on hyper-v host
      
      ```
      $dnsClient = Get-DnsClient | Where-Object {$_.InterfaceAlias -eq "Ethernet" }
      Add-DhcpServerv4Scope -Name "Migrate" -StartRange 192.168.1.1 -EndRange 192.168.1.254 -SubnetMask 255.255.255.0 -State Active
      Add-DhcpServerv4ExclusionRange -ScopeID 192.168.1.0 -StartRange 192.168.1.1 -EndRange 192.168.1.15
      Set-DhcpServerv4OptionValue -DnsDomain $dnsClient.ConnectionSpecificSuffix -DnsServer 168.63.129.16
      Set-DhcpServerv4OptionValue -OptionID 3 -Value 192.168.1.1 -ScopeID 192.168.1.0
      Set-DhcpServerv4Scope -ScopeId 192.168.1.0 -LeaseDuration 1.00:00:00
      Restart-Service dhcpserver
      ```
	 3. Ensure no VLAN ID ise selected in VM properties.

	 4. Disable network adaptor inside the appliance vm and enable it again.
