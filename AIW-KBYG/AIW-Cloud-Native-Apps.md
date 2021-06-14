# Cloud Native Apps : Developer Edition

### Known Issues and workarounds

1. Instructor should make sure that the attendees follow the **lab guide** provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guide and MCW repo lab guide. 

1. Attendees should make sure that they will go through every instruction properly while performing the before hands-on-lab. If at all the lab guide is not followed correctly, attendees will be facing issues in next part of the lab. 

1. The Azure cloud shell can be unresponsive at times, we would suggest you to restart the cloudshell and try again.

1. Yaml files 

   While **editing or inserting** the content into the yaml files, attendees should make sure they read the instructions properly and edit the files accordingly. It is better to cross check the files once, after editing and before saving them. 

1. If attendee’s session to build agent vm gets disconnected,  

   To reconnect to the vm, follow the instruction provided in the before hands-on-lab. 

    1. From Environment details page go to **Command to Connect to Build Agent VM** copy the ssh key and paste in cloud shell. 
    2. In the cloud shell output, paste the ssh key that you copied earlier enter **yes** when prompted. 
    3. Enter the Buid Agent VM password provided in environment details, you will be connected to Build Agent VM. 

1. Issue in before hands-on-lab task 3 step13 

    - When the attendee faces an issue while pushing the changes to the master branch, make sure the GitHub repo URL and the provided credentials are correct. Then ask the attendee to rerun the command **git push -u origin master** to push the changes. 

1. Issues in before hands-on-lab task 5 due to unsuccessful cloning of **Fabmedical** repo. 

    - Ask attendee to verify that whether he had cloned the **Fabmedical** repository properly. If   not, ask the attendee to run the command,  **git clone <GITHUB\_REPOSITORY\_URL>** to clone the **Fabmedical** repo and perform the step again. 

1. Before hands-on-lab task 6 step 17: 

   - If attendee get **no such file or directory** error, run the command  **ng build** , and retry step 17 
   
1. Before hands-on-lab task 11 step 15:  

   - If the Workflow execution fails follow the below instruction to resolve the issue. 
   
        - Make sure that attendee has provided the correct values for resourceGroupName, containerRegistryName and containerRegistry correctly. Then ask attendee to run the workflow again. 
 
   Even after providing the correct values if workflow fails,follow the below steps: 
   
     - Go to cloud shell and open content-web.yml by running the command vi content-web.yml.   
     - In the browser open a new tab and navigate to <https://raw.githubusercontent.com/CloudLabs-MCW/MCW-Cloud-native-applications/fix/Hands-on%20lab/content-web.yml>.   
     - Copy the content till the line ${{ env.containerRegistry }}/${{ env.imageRepository }}:latest, switch back to cloud shell and replace the existing content with the copied content. Make sure to replace [SUFFIX] with your DeploymentId.   
     - Now redo the steps from 10-14.      
    
1. Issue in Exercise 1 Task 2 Step 4 

   When adding migration project if attendee gets the error the connection timed out. Possible reasons for this include 

     - the address and/or port was not correct, or the server is not running. its temporary issue wait for 5-10 minutes then retry again 
     - The mongodb might not be running, run the following command on the build VM to start the DB.
       
       ```docker container start mongo``` 


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
