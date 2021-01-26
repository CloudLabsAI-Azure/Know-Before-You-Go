

##### How much time does the environment take to get deployed? 

The approximate Duration for deploying a single environment would be 35 minutes. 

### Resources that are provided as pre-requisites. 

Once the attendee login to the Azure portal, following are the Pre-deployed resources that are provided to the attendees to perform the lab. 

   - Resource Group: hands-on-lab-UniqueID 
   - Storage account: contosoUniqueID 
   - Virtual machine (VM): LabVM-UniqueID  
   - SQL VM: Sql2008-UniqueID 
   - Azure SQL Database: ContosoInsurance 
   - Azure Database Migration Service (DMS): contoso-dms-UniqueID 
   - Azure App Service Plan: contoso-asp-UniqueID 
   - App Service (Web App): contoso-web-UniqueID 
   - App Service (API App): contoso-api-UniqueID 
   - Function App: contoso-func-UniqueID 
   - API Management: contoso-apim-UniqueID 
   - Key Vault: contoso-kv-UniqueID 
   - Azure Cognitive Search: contoso-search- 
   - Azure Cognitive Services account: cog-services-UniqueID 
   - Virtual Network: vnet-UniqueID 
   - Networksecuritygroup: jbVirtualMachineName-nsg, sqlVirtualMachineName-nsg 
   - NetworkInterfaces : jbVirtualMachineName-nic, sqlVirtualMachineName-nic 
   - publicIpAddress : jbVirtualMachineName-ip, sqlVirtualMachineName-ip 

 - In the upper left corner of the portal window, click the toggle menu icon and then click on **Resource groups,** then select the **hands-on-lab-Uniqueid** resource group and view the pre-deployed resources**.** 

### What do the attendees get when they sign up for the environment?  

- As soon as attendee’s environment is deployed, he will be able to see the Lab Description page.  



![](appmod.001.png) 



- From the Environment Details tab, attendees can find the Azure Credentials, Virtual Machine Credentials, Service Principal details and other details that are required to perform the lab. 

![](appmod.002.png) 

- Scroll down on the Environment Details page and click on the LabVM**-Suffix**   button to login to the Lab VM. 



![](appmod.003.png) 



- Then attendee will be able to see a virtual machine in the left to perform the lab and a lab guide in the right which need to be followed throughout the lab. 



![](appmod.004.png) 



- Scroll down on the Environment Details page and click on the **GO TO SQL2008-Suffix** button to login to the SQL server VM.  



![](appmod.003.png) 



- Then attendee will be able to see a virtual machine in the left to perform the lab and a lab guide in the right which need to be followed throughout the lab. 



![](appmod.005.png) 

- Attendee can see the number on lab guide bottom area to switch to different exercises of lab guide.  
- Attendee can also navigate to previous and next exercise using **Previous** and **Next** button. 



![](appmod.005.png) 





- From the Virtual Machines tab, attendee can find the available virtual machines, their status (running, pending or deallocated), Uptime, DNS name and can also perform some actions on them. 



![](appmod.006.png)  



- Attendee can also perform the following operations on the virtual machine. 



                 1. Start 

                 2. Restart 
     
                 3. Stop and 

                 4. Open the virtual machine in new tab. 



![](appmod.007.png) 



- From the Lab Validation tab, attendees can run validation for each exercise after performing it. 



![](appmod.008.png) 





### Lab Contents 



**Exercise 1: Migrate the on-premises database to Azure SQL Database** 

In this exercise, attendee will use the Microsoft Data Migration Assistant (DMA) to assess the ContosoInsurance database for a migration to Azure SQL Database.  

The assessment generates a report detailing any feature parity and compatibility issues between the on-premises database and Azure SQL Database. 


**Exercise 2: Post upgrade database enhancements** 

In this exercise, attendee will explore through the some of the security features of Azure SQL Database, and review some of the security benefits that come with running your database in Azure.  


**Exercise 3: Configure Key Vault** 

In this exercise, attendee will configure Azure Key Vault, which securely stores application secrets for the Contoso web and API applications, once migrated to Azure. 

**Exercise 4: Deploy Web API into Azure App Services** 

In this task, attendee will apply application settings to the Web API using the Azure Portal. Once the application settings have been set, you deploy the Web App and API App into Azure from Visual Studio. 

**Exercise 5: Deploy web application into Azure App Services** 

In this exercise, attendee updates the Contoso.Web web application to connect to your newly deployed API App by adding API App URL to Web App Application settings and then deploy the web app into Azure App Services.** 

**Exercise 6: Upload policy documents into blob storage** 

In this exercise, attendee will provide a storage account to store the files in a blob container then provides a way to bulk upload their existing PDFs 

**Exercise 7: Create serverless API for accessing PDFs** 

In this exercise, you create an Azure Function to enable an API solution that allows the users of Contoso application to retrieve their policy documents directly from their Azure Storage account using serverless technologies. 

**Exercise 8: Add Cognitive Search for policy documents** 

In this exercise, attendee will configure the cognitive search for the policies blob storage container which provides the ability to perform full-text searching on policy documents. 

**Exercise 9: Create an app in PowerApps** 

In this exercise, attendee will a new app in PowerApps, which connects to the ContosoInsurance database and performs basic CRUD (Create, Read, Update, and Delete) operations against the Policies table. 



### Lab validation

After performing each exercise, the attendees are asked to run validation for the provided tasks to ensure that the expected output is obtained. 

1. Expand lab validation details and click on validate button. 



![](appmod.009.png) 



2. Attendees can find the validation status either Succeeded or failed under status tab 

`                  `If the validation fails, it will give the error message regarding why the validation has failed so that attendee can find the mistake which he committed and rectify it accordingly. 



`   `![](appmod.010.png) 



**Help Tab** 





- Expand **More** button on the right and click on **Help**.  

![](appmod.012.png) 



- From Help tab, attendees can find the common issues such as copy-paste, pop-up visibility issues and solutions to resolve them. 



![](appmod.013.png) 


**Split Window** 



Split window will open the lab guide in new Window by providing the only virtual machine on the current window. 



![](appmod.014.png) 

**Collapse Window** 



Collapse button will collapse the lab guide window and provides the full view of the virtual machine.  



![](appmod.014.png) 



Attendee can get back the lab guide when needed by clicking on Expand button. 





![](appmod.004.png) 







Average time taken to complete the lab: 8 hours 





### Known Issues/Workarounds 





**FAQ’S**: 



How to access lab environment 



- Instructor share the bit.ly link and activation code during the event to attendees. 

`             `DO NOT share the activation details prior to session (Lab Start time) 

- All attendees activate the lab instance using the same activation code. 

` `![](appmod.016.png) 



- Attendee will navigate to the bit.ly link and provide the required details. 
- Its mandatory to give company email address and actual organization name. 

![](appmod.017.png) 



- Once lab instance is assigned, details are also sent to attendee via email from [noreply@cloudlabs.ai 
  ](mailto:noreply@cloudlabs.ai) 
1. Once attendee register using Lab activation details, he will click on Launch Lab to get started with the lab. 



![](appmod.018.png) 


2. Once the deployment is succeeded, attendee will get the Lab description page with Azure Credentials**,** Virtual Machine Credentials, Service Principal details and **other details that are required to perform the lab**, click on **GO TO SQL2008-Suffix** button to login to the SQL server VM and start with lab.   



` `![](appmod.001.png) 



3. Attendee will get the screen with the lab guide, Environment Details (Azure Credentials), etc. on the Right Side and Virtual Machine on the Left. 

` `![](appmod.005.png) 





How to find the **UniqueID** Value: 

Attendee can find the UniqueID value by navigating to **Environment Details** page then selecting Azure Credentials tab. 



![](appmod.019.png) 





How to find the **SERVICE PRINCIPAL** Details: 

Attendee can find the service principal details by navigating to **Environment Details** page then selecting Service Principal tab. 



![](appmod.020.png) 





