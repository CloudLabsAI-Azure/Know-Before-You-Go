# Infrastructure Migration

### RDP OVER HTTPS  

Rdp over https is a feature which allows attendees to access the virtual machine over the internet. This eliminates the need of logging in into the vm by attendees.   

With RDP OVER HTTPS and integrated doc rendering, attendees will be able see the virtual machine and lab guide on the same screen which makes easier to perform the lab.  

` `![](Infrastrure%20Migration.001.png) 

### VM Start/Stop  

Attendees can start/stop the Virtual Machine from the Virtual Machine tab. We have provided button to start/stop VM under Actions.  

` `![](Infrastrure%20Migration.002.png) 

### Instructor Azure Portal Access 

1. Instructor has access to all attendees Resource groups and resources that are pre-deployed or deployed by attendee as a part of the lab. 
1. Instructor can login to the Azure portal with the credentials identified before and will be able to view the resources of all attendees. 

       ![](Infrastrure%20Migration.003.jpeg) 

      ![](Infrastrure%20Migration.004.png) 

1. Since each attendee is assigned with a six-digit Suffix, it is easy for the instructor to view the resources of a particular attendee.  
    
    To find the attendees details:  
    
        - From the Cloud Labs portal home page, Click on **On Demand Labs** select the event ODL then click on user's tab from actions. From here, instructor can find the list of attendees with their deployment id and deployment details for each user. 
        - From the list of attendees, instructor can pick the Suffix of the desired attendee and can view the resources from the Azure portal. 

## How much time does the environment take to get deployed? 

The approximate Duration for deploying a single environment would be 20 minutes. 

## What do the attendees get when they sign up for the environment.  

1. As soon as the attendee’s environment is deployed, he will be able to see a virtual machine on the left which will be used to perform the lab. 

 1. On the right, Attendee will be able to find 

     1. A lab guide, which should be followed to perform the lab.  

          - Attendee can see the number on lab guide bottom area to switch to different exercises of lab guide.  

          - Attendee can also navigate to previous and next exercise using Previous and Next button. 
             
         ![Cloudlabsportal](./images/AIAD-Environment1.png "Environment") 
           
     1. Environment Details which include user credentials (Azure Credentials), Virtual Machine Credentials and other details. 
     
         ![Cloudlabsportal](./images/AIAD-Environment2.png "Environment") 

     1. Virtual Machines tab, attendee can find the available virtual machines, their status (running, pending or deallocated), Uptime and can also perform some actions on them.

         ![Cloudlabsportal](./images/AIAD-Environment3.png "Environment") 

          - Attendee can also perform the following operations on the virtual machine. 

               1. Start 

               2. Restart and

               3. Stop  

          ![Cloudlabsportal](./images/AIAD-Environment4.png "Environment") 
          
     1. From the Lab Validation tab, attendees can run validation for each exercise after performing it. 

          ![Cloudlabsportal](./images/AIAD-Environment5.png "Environment")  

### Lab validation


After performing each exercise, the attendees are asked to run validation for the provided tasks to ensure that the expected output is obtained. 

1. Expand lab validation details and click on validate button. 

    ![Cloudlabsportal](./images/labvalidation1.1.png "labvalidation")

2. Attendees can find the validation status either Succeeded or failed under status tab 

     - If the validation fails, it will give the error message regarding why the validation has failed so that attendee can find the mistake which he committed and rectify it accordingly. 

    ![Cloudlabsportal](./images/labvalidation2.png "labvalidation")

### Help Tab

1. Expand **More** button on the right and click on **Help**.  

    ![Cloudlabsportal](./images/helptab1.png "Helptab")
    
2. From Help tab, attendees can find the common issues such as copy-paste, pop-up visibility issues and solutions to resolve them. 

    ![Cloudlabsportal](./images/helptab2.png "Helptab")
   
   
### Split Window


- Split window will open the lab guide in new Window by providing the only virtual machine on the current window. 

    ![Cloudlabsportal](./images/splitwindow.png "splitwindow")


### Collapse Window

1. Collapse button will collapse the lab guide window and provides the full view of the virtual machine.  

    ![Cloudlabsportal](./images/collapsewindow.png "collapsewindow")
    
2. Attendee can get back the lab guide when needed by clicking on Expand button. 

    ![Cloudlabsportal](./images/collapsewindow1.png "collapsewindow") 


**Average time taken to complete the lab: 8 hours** 

## Resources that are provided as pre-requisites. 

Once the attendee logs in to the Azure portal, the following are the Pre-deployed resources that are provided to the attendees to perform the lab. 

- Resource Groups: 
- AzureMigrateRG 
- SmartHotelDBRG 
- SmartHotelHostRG 
- SmartHotelRG and 
- BastionRG 
- NetworkWatcherRG 

- Resources deployed in SmartHotelHostRG : 

- Virtual machine:  SmarthostSuffix 
- Virtual Network: smarthotelhostvnet, DMSvnet 
- Networksecuritygroup: smarthotelhostnsg 
- NetworkInterfaces: smarthotelhostnic 
- publicIpAddress: smarthotelhostip 

In the upper left corner of the portal window, click the toggle menu icon and then click on **Resource groups,** then select the** SmartHotelHostRG resource group and view the pre-deployed resources**.** 

**LAB CONTENTS** 

**Exercise 1: Discover and assess the on-premises environment** 

- In this exercise, attendee will use **Azure Migrate: Server Assessment** to assess the on-premises environment.  
- This includes selecting Azure Migrate tools, deploying the Azure Migrate appliance into the on-premises environment, creating a migration assessment, and using the Azure Migrate dependency visualization. 

**Exercise 2: Migrate the Application Database** 

- In this exercise, attendee will migrate the application database from the on-premises Hyper-V virtual machine to a new database hosted in the Azure SQL Database service. 
- Attendee will use the Azure Database Migration Service to complete the migration, which uses the SQL Server Data Migration Assistant for the database assessment and schema migration phases. 

**Exercise 3: Migrate the application and web tiers using Azure Migrate: Server Migration** 

- In this exercise, attendee will migrate the web tier and application tiers of the application from on-premises to Azure using **Azure Migrate: Server Migration**. 
- Having migrated to the virtual machines, attendee will reconfigure the application tier to use the application database hosted in Azure SQL. This will enable you to verify that the migration application is working end-to-end. 

**Lab validation** 



After performing each exercise, the attendees are asked to run validation for the tasks provided to ensure that the expected output is obtained. 



1. Expand lab validation details and click on the validate button. 



![](Infrastrure%20Migration.012.png) 



2. Attendees can find the validation status either Success or failed under status tab. 



- If the validation fails, it will give the error message regarding why the validation has failed so that the attendee can find the mistake which he committed and rectify it accordingly. 



![](Infrastrure%20Migration.013.png) 





Average time taken to complete the lab: 8 hours 





Known issues 



Important!! 

Whenever attendee is asked to provide value for **SUFFIX**, it should be replaced with value which can be found from the Environment Details page. Not providing the SUFFIX value will lead to **Deployment issues** while deploying new resources. 

Wherever attendee is asked to provide value for **Location** same as your Azure SQL Database, make sure to select the same region because selecting the different region will not allow the replication and migration of resources. 



Exercise1 Task2 Step2: 



If an attendee is not able to see the virtual machines in the Hyper-V manager  



![](Infrastrure%20Migration.014.png) 



he can wait for 5-10 minutes and refresh the browser the attendee will be able to see the 4 virtual machines in the Hyper-V manager. 



FAQ’s 



How to access lab environment 



- Instructor share the bit.ly link and activation code during the event to attendees. 

`             `DO NOT share the activation details prior to session (Lab Start time) 

- All attendees activate the lab instance using the same activation code. 



` `![](Infrastrure%20Migration.015.png) 



- Attendee will navigate to the bit.ly link and provide the required details. 
- Its mandatory to give company email address and actual organization name. 

![](Infrastrure%20Migration.016.png) 

- Once lab instance is assigned, details are also sent to attendee via email from [noreply@cloudlabs.ai 
  ](mailto:noreply@cloudlabs.ai) 
1. Once attendee register using Lab activation details, he will click on Launch Lab to get started with the lab. 



![](Infrastrure%20Migration.016.png) 


2. Once the deployment is succeeded, Attendee will get the screen with the lab guide, Environment Details (Azure Credentials), etc. on the Right Side and Virtual Machine on the Left. 

![](Infrastrure%20Migration.016.png)  







How to find the **SUFFIX** Value: 

Attendee can find the SUFFIX value by navigating to **Environment Details** page. 



![](Infrastrure%20Migration.016.png) 













**Resource Deployment Time** 

Following are the resources along with deployment duration that are deployed as a part of the lab. 



Azure migrate Project: 30 secs 

Log Analytics workspace: 30 - 60 secs 

SQL database: 3 - 5 minutes 

Azure Database Migration Service: 15-20 minutes 

Private endpoint: 2 - 3 minutes 

Storage Account: 30 - 60 secs 

Virtual Network: 10 – 20 secs 

Replication of Virtual machines: 10 – 15 mins 

Migration of Virtual machines: 5 – 10 mins 

Bastion: 4 – 5 minutes 



