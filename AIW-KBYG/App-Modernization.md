# App Modernization

#### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/db3f19de-8f56-41bf-af3c-a8ebf69864ee)

## Known Issues and workarounds 

- [Known issues](#known-issues)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

## Known issues

1. **Exercise 4 -> Task 2 -> Step No 4**

    If attendee encounters below issue when connecting to SQL sever from Data Migration Assistant, it is because of incorrect password.
    
    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/appmodissue-4.png?raw=true)  
    
    To fix this issue, enter the correct password and try connecting to the server again, make sure no extra spaces are copied when you paste the passowrd value.

2. **Azure API issue**: 

   - Due to recent changes in Azure API's, Azure API's are taking some additional time to fetch the details of the resources. The validation steps for the lab may fail at first, but if you re-run them after 30-45 minutes, they will get succeed if there are no configuration related issues with the lab steps you performed. 
