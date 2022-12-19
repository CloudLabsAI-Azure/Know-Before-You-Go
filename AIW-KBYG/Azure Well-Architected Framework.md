# Azure Well-Architected Framework

##### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/a9dbe192-7e71-45a9-8030-f32ee7d5e6c9)

### Known Issues and workarounds
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

1. **Exercise 2 -> Task 3 -> Create a Logic App ->Step No 14**

   - If you face the **Sign in issue** while loggin into Azure, please make sure you are using the edge browser and re-perform the task again.

   ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/logicapp-issue.png?raw=true) 

2. **Azure API issue**: 

    - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources. The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.

    - The attendees may face issues while trying to access the environment.
    - they can check to see if the VM is in the running state, if not they can start it from the Virtual machine tab. 
    - It could also be due to a duplicate window open in another browser, we suggest closing all windows and trying again. Or using a private window and clearing the cookies. 
