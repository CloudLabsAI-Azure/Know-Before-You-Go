# Azure Immersion Workshop: AI

Instructor should make sure that the attendees follow the **lab guide** provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guides in GitHub repos. 

##### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/0f7131b7-1208-4051-a32b-44afc42fbf14)

### Known Issues and workarounds
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Known issues in Lab Steps

1. Azure API issue: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.

2. [Lab 2a - Task 6 Using the Form Recognizer Studio](https://github.com/CloudLabsAI-Azure/ai-in-a-day/blob/FY-23-AI-Updates/03-knowledge-mining/2a-document-processing-and-summarization.md)

   **Issue in Form Recognizer Studio while creating a Custom model project**.

   - In some cases user may face an issue to select Storage account in Connect training data source pane.    
   - **This is an intermittent issue**.

   **Solution:**
    
   - Signout and Signin from the Form Recognizer Studio with the given user credentials and re-perform the task from Step-8.
   - If you are still facing the issue, then delete the **Resource sharing (CORS)** policy which you have configured at Step-4 of the same task and re-perform the task from Step-4.

 3. [Lab 4: Hand-on-Lab > Task 4 - Configure the "COVID cases by age group" Metrics Advisor data feed](https://github.com/CloudLabsAI-Azure/ai-in-a-day/blob/FY-23-AI-Updates/05-metrics-advisor/05-metrics-advisor-new.md)

    **Issue with Get Started button in Metric Advisor workspace in Step-3**.
    
    - This is an intermittent issue with the Azure Product. If faced during the lab experience please mail to [CloudLabs Support](cloudlabs-support@spektrasystems.com) or contact the Instructor.
