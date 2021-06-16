# CloudLabs Shadow

**CloudLabs Shadow** is CloudLabs embedded shadow feature, which normally shadow the pre-deployed attendees Virtual Machine.
  - Most of the labs hosted on CloudLabs has LabVM/JumpBox with pre-configured tools required for the lab, where attendees performs the complete lab.
  - Attendees virtual machine (LabVM/JumBox) can be shadowed and monitored by Instructors in real time.
    * By shadowing the attendees virtual machines (VMs) instructors can help attendees to look and help in troubleshooting the issues. 
    * CloudLabs Support team can assist attedees and instructors during dryrun and actual workshop.
  - It will not disconnect the attendees RDP (Remote Desktop Connection). While instructors are shadowing the session, attendees wil not be disconnected from the VM.

### Using CloudLabs Shadow:
Now, shadowing the attendees' VM is single button ahead. Here are the steps for shadowing the attendees VM using CloudLabs Shadow.
1. Login to https://admin.cloudlabs.ai with your work account (alias@microsoft.com or alias@partner.com).
1. Upon login, on demand lab will be available for management.
    - Ensure to select the right CloudLabs tenant **Microsoft – Azure Immersion Workshop(AIW)** (1)
    - Navigate to **On Demand Labs** (2)
    - On **[Instructor Cloud Details]()** (3) Azure Credentials can be found. With these credentials instructors can access all the attendee’s Azure environment. (3)
    - On **Users** (4) tab already registered users can be found, and new registrations can be added in bulk. Also, lab environment and shadowing can be launched from here.
   ![](.././media/cs-001.png)
   
#### Instructor Cloud Details: 
Azure Credentials are available at instructor cloud details or i button. These Azure credentials will have access to all attendees Azure environment and Instructor can manage the Azure resources of attendees from a single Azure Account.
  ![](.././media/cs-002.png)
  
#### Users
Navigate to user's tab from actions. Check Deployment ID (DID) for each User (Email).
  - Deployment details for user (you can use azure credentials from this page to access attendee cloud environment).
  - You can manage attendees from this page.
  - Add / Remove attendees.
  - Each attendee is assigned a six-digit unique id to identify lab resource groups and jump VMs.
![](.././media/cs-003.png)

#### Shadow Attendee's Virtual Machine
1. From **Users** tab click on Launch VM Shadow a **BINOCULAR** icon to shadow the attendee's VM and let us call this Instructor login. A virtual machine session will open in new tab of web browser.
   ![](.././media/cs-004.png)
1. You will see a Remote Desktop Connection automatically opens (1), that is attendees session shadow. You can Maximize the Shadow session by clicking on maximize icon (2).
   ![](.././media/cs-005.png)
1. This is possible that you may not find attendees shadow session open in the instructor login due to following reasons.
   - Attendees is not connected to the VM yet. If attendee did not access lab environment yet that mean attendee need to connect VM then only it will be visible in Instructor login.
     ![](.././media/cs-006.png)
     
   - Attendee disconnected the virtual machine (VM). In this case inform attendee to connect to the VM if needed.
     ![](.././media/cs-007.png)
     
   - If attendee connects back to the VM, shadow session will open automatically in Instructor login.
  
1. If you close the attendees shadow session accidentally, re-launch it from **Shadow Lab User VM** shortcut created on desktop 🖥.
   ![](.././media/cs-008.png)
  
  

 


