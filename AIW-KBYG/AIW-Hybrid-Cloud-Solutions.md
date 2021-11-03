# Azure Immersion Workshop: Hybrid Cloud Solutions


### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)


### Know issues in Lab Steps

1. Issue with Ubuntu K8s VM Start:

	**ubuntu-k8s failed to restore**
	
	Solution: Right click on the **ubuntu-k8s vm** from the Hyper-V Manager and then click on Delete Saved State and then start the VM from the Hyper-V Manager


1. If **LabVM** opens on full screen, then you can **Restore Down** the window. 

    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-9.png?raw=true) 

1.  Split the Window from lab environment page to open the Lab guide in Separate Window. 

    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-10.png?raw=true) 

1.  Now, copy the lab environment URL from the list and open that inside the VM itself and then use the Vm on full screen. 

    ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-11.png?raw=true) 
    
1. Azure API issue: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.
