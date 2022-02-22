# Azure Immersion Workshop: DevOps with GitHub

Instructor should make sure that the attendees follow the **lab guide** provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guide and MCW repo lab guide.

##### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/555df165-4549-44b1-b557-5eca8826cdf1)

### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Known issues in Lab Steps 

1. #### Exercise 1 Task 3 Step 2:

    - While running the docker-compose YAML files, make sure that the docker desktop is in running state.

    - If user face an issue while running above command with respect to default daemon configuration, open docker desktop and click on **Troubleshoot** icon at the right corner and select **Restart** to restart the docker desktop. It might take upto 5 minutes for restarting and rerun the command once restart is completed.

      ![image](https://github.com/Kalyani7744/Know-Before-You-Go/blob/main/Labs/images/Dockerrestart.png?raw=true)

2. #### Azure API issue: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.
