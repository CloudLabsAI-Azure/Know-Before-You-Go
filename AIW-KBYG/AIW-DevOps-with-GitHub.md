# Azure Immersion Workshop: DevOps with GitHub

### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Know issues in Lab Steps 

**Note :** We are providing github accounts with codespace access, Users will get the github credentials on Lab Environment Page.

1. Module 1 Task DEVWF-T004 step 6 if you get merge conflicts open a PowerShell Terminal in your GitHub Codespace and run the below commands.

   ```
   git add .
   git commit -m "Resolved merge conflict by incorporating both suggestions."
   ```
   
2. Module 3 Task CLOSELOOP-T003 if pipeline fails with error invalid token, navigate to project settings tab and delete the docker registry connection. Now re-perfom the setup service connection steps again.

   https://github.com/CloudLabsAI-Azure/AIW-DevOps/blob/main/Challenges/Module3-ClosingTheFeedbackLoop/Step-By-Step/CLOSELOOP-T003-SBS.md#setup-service-connection-in-your-azure-devops-project
