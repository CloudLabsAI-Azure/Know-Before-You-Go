# Azure Immersion Workshop: Hybrid Cloud Solutions

##### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/7a1ad116-d7a9-4cbf-a4a0-dbb5b3b66906)

### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

### Know issues in Lab Steps

1. Issue with Ubuntu K8s VM Start:

	**ubuntu-k8s failed to restore**
	
	Solution: Right click on the **ubuntu-k8s vm** from the Hyper-V Manager and then click on Delete Saved State and then start the VM from the Hyper-V Manager
   
1. Azure API issue: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.
