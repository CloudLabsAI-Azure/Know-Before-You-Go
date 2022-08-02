# Azure Immersion Workshop: Hybrid Cloud Solutions

##### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/7a1ad116-d7a9-4cbf-a4a0-dbb5b3b66906)

### Known Issues and workarounds
- [Known issues in Lab Steps](#Known-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

### Known issues in Lab Steps

1. Issue with Ubuntu K8s VM Start:

	**ubuntu-k8s failed to restore**
	
	Solution: Right click on the **ubuntu-k8s vm** from the Hyper-V Manager and then click on Delete Saved State and then start the VM from the Hyper-V Manager
   
1. Azure API issue: 

   - Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.

1. AKSHCI deployment issue in HOL4-Azure Stack HCI:
	
   - In HOL4 Azure Stack HCI-Exercise 2, The deployment of AKSHCI may fail because the kubernetes does not support the nested virtualisation and the deployment can lead to timeout thoughout the AKS-HCI code. Below is the information provided in MS docs:
   
	>Note: Nested virtualization should only be used for development purpose when no other solution is available. When nested virtualization is used in Hyper-V, performance is reduced by 30%. When Hyper-V is nested inside another Hyper-V VM, performance is reduced by 80%. Since AKSHCI uses one level of virtualization, creating a multi node environment using nested virtualization results in 80% container performance reduction. This ultimately leads to spurious timeout throughout the AKS-HCI code. Do NOT use in production, it will NOT be supported!
