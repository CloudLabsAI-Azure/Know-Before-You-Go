# Azure Arc Hybrid Cloud Solutioons

## Contents

- [How to navigate to the cloud labs portal](#how-to-navigate-to-the-cloud-labs-portal)
- [How to manage users and Unused instances](#how-to-manage-users-and-Unused-instances)
- [Vm Shadowing](#vm-shadowing)
- [RDP Over Https](#rdp-over-https)
- [VM Start/Stop ](#vm-startstop)
- [Instructor Azure Portal Access ](#instructor-azure-portal-access)
- [What do the attendees get when they sign up for the environment](#What-do-the-attendees-get-when-they-sign-up-for-the-environment)
- [Help Tab](#help-tab)
- [Split Window](#split-window)
- [Collapse Window](#collapse-window)
- [Resources that are provided as pre-requisites ](#resourcesthat-are-provided-as-pre-requisites)
- [Lab Contents](#lab-contents)
- [Lab validation](#lab-validation)
- [Known Issues and workarounds ](#known-issues-and-workarounds)
- [FAQ'S](#faqs)

## How to navigate to the cloud labs portal

- Open any browser and navigate to <https://admin.cloudlabs.ai/>  
- Click on sign in and then sign with Work or School Account.  
- Upon login, on demand lab will be available for management. 

   1. Ensure to select the right Cloud Labs tenant. 
   2. Navigate to On Demand Labs, then you will be able to find event ODL name.  
   3. From here you can find instructor credentials. With this credential you can access all the attendee’s azure environments. 
   4. From Users tab, you can find list of lab users with their deployment id. 
   
 ![Cloudlabsportal](./images/cloulabsportal.png "cloudlabsportal")
 
## How to manage users and Unused instances

- Navigate to user's tab from actions..  
- From here you can find the list of users with their deployment id and deployment details for each user.  
- You can manage attendees from this page  
- Add / Remove attendees  
- Each attendee is assigned a six-digit unique id to identify lab resource groups and jump VMs 

 ![Cloudlabsportal](./images/cloudlabs-users.png "cloudlabsportal")

## Features available to instructors

### Vm Shadowing  

- You can shadow multiple attendee VMs at the same time.  
- Multiple instructors / proctors can shadow same attendee VM concurrently.  
- If you don’t see the username upon clicking “Shadow Session”, student may not have launched their Lab VM yet or is disconnected.  

1. Login to [https://admin.cloudlabs.ai](https://admin.cloudlabs.ai/) with your work account (<alias@microsoft.com> or <alias@partner.com>)   
1. Ensure to select the right Cloud Labs tenant (Microsoft – In a Day)  
1. Navigate to On Demand Labs  
1. Using instructor credentials, you can access all the attendee’s azure environments.  
    - Click on information icon from Actions to get Instructor Azure Credentials  
    - Use this username and password to login to Azure portal and CloudLabs Shadow  
    - Login from a private browser instance (InPrivate or Incognito)  

    ![Cloudlabsportal](./images/cloudlabs-instructor.png "cloudlabsportal") 

1. Navigate to user's tab from actions  
1. You can find the Deployment details for the user here. (you can use azure credentials from this page to access attendee cloud environment)  

   ![Cloudlabsportal](./images/cloudlabs-users.png "cloudlabsportal")
 
   SCREEN CONNECT  

1. Navigate to [https://spektrasystems.screenconnect.com](https://spektrasystems.screenconnect.com/)  
1. Click on Login  

   ![VM shadowing](./images/screenconnect1.png "cloudlabsportal")

1. Login with local account, do not choose Azure AD.  
1. Use same username and password provided for Instructor Access  

    ![VM shadowing](./images/screenconnect2.png "cloudlabsportal")
 
    ![VM shadowing](./images/screenconnect3.png "cloudlabsportal")

1. OTP is sent to your work email account. Check and provide the OTP then Login.  
     - Please be sure to check junk/spam folder.  
     - Email is sent out from <cloud@screenconnect.com>  

    ![VM shadowing](./images/screenconnect4.png "cloudlabsportal")

1. Search for specific DID if needed, right Click on Lab User VM (Identified by DID) and Select Shadow Session  

    ![VM shadowing](./images/screenconnect5.png "cloudlabsportal")

1. Select Login Session – demouser or if you see any other username to connect the VM and click on Join Session 

    >Note: If you only see Console and [Backstage], that means attendee is not connected to VM currently  

    ![VM shadowing](./images/screenconnect6.png "cloudlabsportal")

1. Click on Open ScreenConnect Client and install the required software (One Time).  

    ![VM shadowing](./images/screenconnect7.png "cloudlabsportal")
    
1. Shadow users VM session (without overtaking RDP session).

    ![VM shadowing](./images/screenconnect8.png "cloudlabsportal")
1. You can initiate a private chat with attendee by clicking on messaging icon.

    ![VM shadowing](./images/screenconnect9.png "cloudlabsportal")


### RDP Over Https

- Rdp over https is a feature which allows attendees to access the virtual machine over the internet. This eliminates the need of logging in into the vm by attendees.   

- With RDP OVER HTTPS and integrated doc rendering, attendees will be able to see the virtual machine and lab guide on the same screen which makes easier to perform the lab.  

 ![Cloudlabsportal](./images/AIAD-RdpoverHttps.png "RdpoverHttps")
 
### VM Start/Stop  

- Attendees can start/stop the Virtual Machine from the Virtual Machine tab. We have provided button to start/stop VM under Actions.  

 ![Cloudlabsportal](./images/AIAD-vmstartandstop.png "Vmstartandstop")
 
### Instructor Azure Portal Access 

Instructor has access to all attendees Resource groups and resources that are pre-deployed or deployed by attendee as a part of the lab. 
1. Instructor can login to the Azure portal with the credentials identified before and will be able to view the resources of all attendees. 

   ![Cloudlabsportal](./images/cloudlabs-instructor-1.png "cloudlabs-instructor")
 
   ![Cloudlabsportal](./images/cloudlabsinstructor2.png "cloudlabs-instructor")
 
1. Since each attendee is assigned with a six-digit Suffix, it is easy for the instructor to view the resources of a particular attendee.  

   To find the attendees details:  

     - From the Cloud Labs portal home page, Click on **On Demand Labs** select the event ODL then click on user's tab from actions. From here, instructor can find the list of attendees with their deployment id and deployment details for each user. 
     - From the list of attendees, instructor can pick the Suffix of the desired attendee and can view the resources from the Azure portal. 


## How much time does the environment take to get deployed? 

- The approximate Duration for deploying a single environment would be 60 minutes. 

## The total duration of this lab is 4 hours 

- The attendee will have access to the lab environment for 8 hours, unless notified otherwise. 

## What do the attendees get when they sign up for the environment?

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
          
          
### Help Tab

1. Expand **More** button on the right and click on **Help**.  

    ![Cloudlabsportal](./images/AIAD-Helptab-1.png "Helptab")
    
2. From Help tab, attendees can find the common issues such as copy-paste, pop-up visibility issues and solutions to resolve them. 

    ![Cloudlabsportal](./images/AIAD-Helptab-2.png "Helptab")
   
   
### Split Window


- Split window will open the lab guide in new Window by providing the only virtual machine on the current window. 

    ![Cloudlabsportal](./images/AIAD-splitwindow.png "splitwindow")


### Collapse Window

1. Collapse button will collapse the lab guide window and provides the full view of the virtual machine.  

    ![Cloudlabsportal](./images/AIAD-collapsewindow-1.png "collapsewindow")
    
2. Attendee can get back the lab guide when needed by clicking on Expand button. 

    ![Cloudlabsportal](./images/AIAD-collapsewindow-2.png "collapsewindow") 

## Resources that are provided as pre-requisites

- Once the attendee’s login to the Azure portal, the following are the Pre-deployed resources that are provided to the attendees to perform the lab. 
   - Resource Groups: azure-arc 
   - Resources deployed in Synapse-AIAD-UniqueID: 
   
      - Storage account
      - Virtual Machine - ArcHostVMUniqueID
      - Azure Kubernetes Service 

## LAB CONTENTS 

### Hands-on Lab 1: 

First, let's start by learning how to onboard a virtual machine and Kubernetes cluster, both running on-premises, to Azure Arc, apply a few Azure Policies, enable monitoring, and alerts as well as Integrate Azure Security Center and Azure Sentinel to your on-premises resources. You’ll also be able to deploy an SQL Server on the VM, connect it to Arc and explore SQL Assessments for this resource.

### Hands-on Lab 2: 

In this lab, you’ll learn to deploy GitOps configurations to the Kubernetes cluster that you onboarded to Arc earlier and enable Azure Policy add-on for Kubernetes to the same cluster.

### Hands-on Lab 3: 

In this lab, you will deploy the Azure Arc data controller, Azure SQL Managed Instance & Azure PostgreSQL Hyperscale to an existing Kubernetes cluster.


   
    
## Known Issues and workarounds 

## FAQ’S


### How to access lab environment

1. Instructor share the bit.ly link and activation code during the event to attendees. 

    DO NOT share the activation details prior to session (Lab Start time) 

1. All attendees activate the lab instance using the same activation code. 

    ![Cloudlabsportal](./images/AIAD-Environment7.png "Environment")

1. Attendee will navigate to the bit.ly link and provide the required details. 
1. Its mandatory to give company email address and actual organization name. 

    ![Cloudlabsportal](./images/AIAD-Environment7.1.png "Environment")
        
1. Once lab instance is assigned, details are also sent to attendee via email from [noreply@cloudlabs.ai 
  ](mailto:noreply@cloudlabs.ai) 
1. Once attendee register using Lab activation details, he will click on Launch Lab to get started with the lab. 

   ![Cloudlabsportal](./images/AIAD-Environment6.png "Environment")
    
1. Once the deployment is succeeded, attendee will get the screen with the lab guide, Environment Details (Azure Credentials), etc. on the Right Side and Virtual Machine on the Left. 

 ![Cloudlabsportal](./images/AIAD-RdpoverHttps.png "RdpoverHttps") 

### How to find the **UniqueId** Value:

- Attendee can find the UniqueId value by navigating to **Environment Details** page. 

    ![Cloudlabsportal](./images/AIAD-suffix.png "Environment")

