# Azure Immersion Workshop: AI

Instructor should make sure that the attendees follow the **lab guide** provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guides in GitHub repos. 

##### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/3dbb2116-28d1-4a47-9e52-25969482acb8)

### Known Issues and workarounds
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Known issues in Lab Steps

1. Azure API issue: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.

2. [Lab 2a - Task 6 Using the Form Recognizer Studio](https://github.com/CloudLabsAI-Azure/ai-in-a-day/blob/FY-23-AI-Updates/03-knowledge-mining/2a-document-processing-and-summarization.md)

   **Issue in Form Recognizer Studio while creating a Custom model project**.

   - In some cases user may face an issue that unable to select Storage account in Connect training data source pane.    
   - **This is an intermittent issue**.

   **Solution:**
    
   - Signout and Signin from the Form Recognizer Studio with the given user credentials and re-perform the task from Step-8.
   - If you are still facing an issue, then delete the **Resource sharing (CORS)** policy which you have configured at Step-4 of the same task and re-perform the task from Step - 4.
