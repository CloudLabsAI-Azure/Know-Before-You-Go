# Cloud Native Applications - Developer Edition

### Known Issues and workarounds

1. Instructor should make sure that the attendees follow the **lab guide** provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guide and MCW repo lab guide. 

1. Attendees should make sure that they will go through every instruction properly while performing the before hands-on-lab. If at all the lab guide is not followed correctly, attendees will be facing issues in next part of the lab. 

1. Yaml files 

   While **editing or inserting** the content into the yaml files, attendees should make sure they read the instructions properly and edit the files accordingly. It is better to cross check the files once, after editing and before saving them. 

1. If attendee’s session to build agent vm gets disconnected,  

   To reconnect to the vm, follow the instruction provided in the before hands-on-lab. 

    1. From Environment details page go to **Command to Connect to Build Agent VM** copy the ssh key and paste in cloud shell. 
    2. In the cloud shell output, paste the ssh key that you copied earlier enter **yes** when prompted. 
    3. Enter the Buid Agent VM password provided in environment details, you will be connected to Build Agent VM. 

1. Issue in before hands-on-lab task 3 step13 

    - When the attendee faces an issue while pushing the changes to the master branch, make sure the GitHub repo URL and the provided credentials are correct. Then ask the attendee to rerun the command **git push -u origin master** to push the changes. 

1. Issues in Exercise 1 due to unsuccessful cloning of **Fabmedical** repo. 

    - Ask attendee to verify that whether he had cloned the **Fabmedical** repository properly. If   not, ask the attendee to run the command,  **git clone <GITHUB\_REPOSITORY\_URL>** to clone the **Fabmedical** repo and perform the step again. 

1. Exercise1 Task1 Step17: 

   - If attendee get **no such file or directory** error, run the command  **ng build** , and retry step 17 
   
1. Exercise1 task9:  

   - If the Workflow execution fails follow the below instruction to resolve the issue. 
   
        - Make sure that attendee has provided the correct values for resourceGroupName, containerRegistryName and containerRegistry correctly. Then ask attendee to run the workflow again. 
 
   Even after providing the correct values if workflow fails,follow the below steps: 
   
     - Go to cloud shell and open content-web.yml by running the command vi content-web.yml.   
     - In the browser open a new tab and navigate to <https://raw.githubusercontent.com/CloudLabs-MCW/MCW-Cloud-native-applications/fix/Hands-on%20lab/content-web.yml>.   
     - Copy the content till the line ${{ env.containerRegistry }}/${{ env.imageRepository }}:latest, switch back to cloud shell and replace the existing content with the copied content. Make sure to replace [SUFFIX] with your DeploymentId.   
     - Now redo the steps from 10-14. 
     
1. Issue while using Kubernetes Dashboard 

   - If attendee lose the connection to Kubernetes dashboard, he should run the command again in Cloud Shell to re-establish the connection.  

   - If the Kubernetes dashboard becomes unresponsive in the browser this is an indication to return cloud shell and check your tunnel or rerun the command. 

   - If attendee is facing the issue as mentioned in the below screenshot. Follow any one of the provided solutions to resolve the issue. 

        ![Cloudlabsportal](./images/Cloudnative-issue.png "Environment") 

       - Then ask the attendee to click on the "user/profile" icon in the upper-right of the dashboard, select "Sign out", then sign back into the K8s dashboard and it will work again.  

      - Restart the cloud shell and rerun the command to establish the connection then browse to the Kubernetes dashboard. 

1. Issue in Exercise 2 Task 2 Step 4 

   When adding migration project if attendee gets the error “the connection timed out. Possible reasons for this include 

     - the address and/or port was not correct, or the server is not running.” its temporary issue wait for 5-10 minutes then retry again 

1. Exercise 5 Task3 Step6: 

   - Even after increasing CPU to 125m, if scaling of pods fails with error “invalid syntax and insufficient CPU”. Follow the below steps. 

