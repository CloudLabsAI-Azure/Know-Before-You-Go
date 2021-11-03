# App Modernization

## Known Issues and workarounds 

- [Known issues](#known-issues)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

## Known issues

1. **Exercise 3 -> Task 1 -> Step No 5**

    If attendee encounters below issue when connecting to SQL sever from Data Migration Assistant, it is because of incorrect password.
    
    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/appmodissue-4.png?raw=true)  
    
    To fix this issue, enter the correct password **Password.1!!** and try connecting to the server again, make sure no extra spaces are copied when you paste the passowrd value.

2. **Exercise 4 -> Task 3 -> Step No 3**

  There is an Inconsistent UI for Azure Web App Deployment Center.  Each Attendee might see a different UI when they access the deployment center within Azure Web App Slot due to which some of the attendees won't be getting a drop down to select the desired .Net Version. Attendee can follow the below instructions to select the desired verison of .Net Core.
     
   1. Select **Configuration** from the left-hand side menu then **General Settings**.

      ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/appmodissue-1.png?raw=true)

   2. On the **General settings** blade, provide the below information under **Stack settings** sections

        - Stack: Select **.Net** from the dropdown.
        - .NET version: Select **.NET Core(3.1,2.1)** from the dropdown.

       ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/appmodissue-2.png?raw=true)

   3. Click on **Save** then **Continue** to save the changes.

       ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/appmodissue-3.png?raw=true)
       
   4. Select **Overview** from the left-hand side menu and click on **Restart** to restart the app.

       ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/media/appmodissue-5.png?raw=true)

   5. Switch to the **Deployment Center** tab, select **GitHub** as the source and select **Authorize** to create the connection between the App Service deployment slot and the GitHub repository.

3. **Azure API issue**: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.
