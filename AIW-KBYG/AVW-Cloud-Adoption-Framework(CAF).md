# Cloud Adoption Framework

In this lab all the exercises are independent to each other.

## Known Issues and workarounds 
1. [Jumpbox/LabVM connectivity/RDP over HTTP issue](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/AIW-KBYG/RDP-over-HTTP-Workaround.md#remote-desktop-functionality-known-issues-)

1. In Exercise 3, template deployments fails sometime. We have seen deleting the all **aks** policies from **Landing Zone** Management group and redeploying the template after deleting all **aks** policy fix the issue most of the time. We have raised issue in Original Git repository [here](https://github.com/Azure/Enterprise-Scale/issues/597) and we are also working on template update to fix this.

1. Exercise 4 Task 3 Step 3 : **Machines to update** 

   - Sometime Machine will take more than 40 minutes to appear on the screen, you have to wait till the VM appear on the screen.

     ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/CAF%202.png)
     
1. Exercise 4 Task 4 Step 3: 

   - We have noted that Log Query window is not being loaded for hours many times.

1. Exercise 4  Task 4 Step 4 : **Logs** in Log Analytics

   - To apprearing the Result, sometime it take more than 1 hour or it will show **No Result Found** than you have to check the **Change Tracking and Inventory checks** and if everything is correct, and if log still not appear than you dont need to wait you can proceed with the lab, there might be delay from the azure end.

     ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/CAF%201.png)
