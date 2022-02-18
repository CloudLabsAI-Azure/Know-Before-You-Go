# Azure Immersion Workshop: Infrastructure Migration

## Known issues and workarounds

- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)
- [Lab guide preview URL](https://experience.cloudlabs.ai/#/labguidepreview/4c14777d-6338-4016-9ac6-ba7b050a4816)

## Know issues in Lab Steps 

1. **Exercise1 -> Task2 -> Step3**: 

   If attendee receives below error while generating the **Azure Migrate project key** in Azure Migrate. In this case go to the Azure Migrate main page and create a new project with different name, select that newly created project and perform the **Step 3 of Task2** again to generate the key.
   
   ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/LOB-issue.png?raw=true)
   
   **Note**: In this case, validations will fail, as the validation is configured to check the discovered servers, Assessments and AssessmentGroup under migrate project **SmartHotelMigrationDID** but attendee will be using different Migrate project in this case.
   

1. **Exercise1 -> Task3 -> Step3**: 

   If attendee receive a prompt asking for credentials after launching the **Azure Migrate appliance configuration wizard** using the shortcut available on the desktop, follow the below instructions:
   
   1. From the Azure Migrate Appliance VM, open IIS manager and select the **Conections** that starts with **WIN**.

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/lob-issue-03.png?raw=true)
      
   1. Now, select **Authentication** under IIS from the home page.

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/lob-issue-04.png?raw=true)
      
   1. Select **Windows Authentication** and click on **Enable** to enable it.

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/lob-issue-05.png?raw=true)
   
   1. Close the **Azure Migrate appliance configuration wizard** and re-launch it using the desktop shortcut.

1. **Exercise1 -> Task3 -> Step17**: 
    
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
     
1. **Exercise2 -> Task3 -> Step16**:    

    If attendee gets below error while connecting to the target SQL database in the process of migrate project creation, you can delete the existing **SmartHotel-DB-for-DMS** endpoint, recreate it and then perform Task3 again.
    
    
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


1. **Exercise3 -> Task9 -> Step6**: 

   If you receive any error while accessing the application using UbuntuWAF VM IP address, then follow the below instructions to access the smarthotel application:
   
   1. Navigate to the **SmartHotelDBRG** resource group, and then to the **SmartHoteldb<inject key="DeploymentID" enableCopy="false" />** database server to update the    Firewall settings.
   1. Under Security, select Firewalls and virtual networks. Set 'Deny public network access' to **No** and 'Allow azure service and resources to access this server' to **yes**, then Save your changes.

      ![](https://raw.githubusercontent.com/Kalyani7744/Know-Before-You-Go/main/media/lob-issue-01.png)
     
   1. Open a new browser tab and paste the IP address into the address bar. Verify that the SmartHotel360 application is now available in Azure.
   
       ![](https://raw.githubusercontent.com/Kalyani7744/Know-Before-You-Go/main/media/lob-issue-02.png)
      
1. **Azure API issue**: 

     - Due to recent changes in Azure API's, Azure API's are taking some additional time to fetch the details of the resources. The validation steps for the lab may fail at first, but if you re-run them after 30-45 minutes, they will get succeed if there are no configuration related issues with the lab steps you performed.
