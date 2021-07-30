# App Modernization

## Known Issues and workarounds 

- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)
- Known issues

**Exercise 4 -> Task 3 -> Step No 3**

  There is an Inconsistent UI for Azure Web App Deployment Center.  Each Attendee might see a different UI when they access the deployment center within Azure Web App Slot due to which some of the attendees won't be getting a drop down to select the desired .Net Version. Atedee can follow the below instructions to select the desired verison of .Net Core.
     
   1. Select **Configuration** from the left-hand side menu then **General Settings**.

   2. On the **General settings** blade, provide the below information under **Stack settings** sections

        - Stack: Select **.Net** from the dropdown**.
        - .NET version: Select **.NET Core(3.1,2.1)** from the dropdown**.

   3. Click on **Save** then **Continue** to save the changes.

   4. Switch to the **Deployment Center** tab, select **GitHub** as the source.

