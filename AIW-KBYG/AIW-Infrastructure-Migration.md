# Infrastructure Migration

## Known issues and workarounds

1. ### Important!! 

   - Whenever attendee is asked to provide value for **SUFFIX**, it should be replaced with value which can be found from the Environment Details page. Not providing the SUFFIX value will lead to **Deployment issues** while deploying new resources. 

   - Wherever attendee is asked to provide value for **Location** same as your Azure SQL Database or same as your resource group, make sure to select the same region because selecting the different region will not allow the replication and migration of resources. 

1. **Exercise1 Task2 Step3**: 

   If attendee receives below error while generating the **Azure Migrate project key** in Azure Migrate. In this case go to the Azure Migrate main page and create a new project with different name, select that newly created project and perform the **Step 3 of Task2** again to generate the key.
   
   ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/LOB-issue.png?raw=true)
   
   **Note**: In this case, validations will fail, as the validation is configured to check the discovered servers, Assessments and AssessmentGroup under migrate project **SmartHotelMigrationDID** but attendee will be using different Migrate project in this case.
   
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
