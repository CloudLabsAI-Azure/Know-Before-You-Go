# Azure Virtual Workshop: Cloud Adoption Framework

### Known Issues and workarounds
- [Know issues in Lab Steps](#know-issues-in-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

#### Know issues in Lab Steps 

1. **Increased time with ARM template deployment:** As compared to the older version of the lab – The ARM template deployment time has been increased and it is mentioned in the lab guide instructions that the deployment of ARM template can take up to 90 minutes as it consists of resources which take time to deploy hence it is expected. You can however proceed to the next Exercise i.e. Exercise 2 on the next page of lab guide and you can come back and check if deployment is succeeded, if it is succeeded then you can resume back to the remaining steps in Exercise 1 and then Exercise 3.

2. **Deployment Fails:** In Exercise 1 Task 1 and step 16, ARM template deployments fails sometimes.

     1. Deployment fails with policy assignments, sometime private DNS endpoint deployment fails. This is a known issue you potentially can run into as described here: https://github.com/Azure/Enterprise-Scale/blob/main/docs/EnterpriseScale-Known-Issues.md#deploying-the-reference-implementation-fails-due-to-policy--cannot-be-found-404

   **Fix deployment**: 
     * Redeploy the template by following the Exercise 1 Task 1
     * If redeploying the template fails again, then cleanup the management groups, policy assignments and resource groups which got deployed as part of ARM tremplate deployment in exercise 1 and task 1. Now, deploy the template again.

  * Sometimes **Landing Zone template** deployment fails with below error.
       
      ```
       {
      "status": "Failed",
      "error": {
        "code": "RoleAssignmentUpdateNotPermitted",
        "message": "Tenant ID, application ID, principal ID, and scope are not allowed to be updated."
        }
       }
       ```
       
    **Fix deployment**: 

      * Navigate to all the **connected subscriptions** under **eslz** management group then **remove** all the role assignments with name **Identity Not Found** by selecting **IAM** from the navigation menu. 
      * Now, redeploy the template by following the Exercise 1 Task 1.
    
3. **Usage of personal GitHub accounts:**
     The attendees will need to have their own GitHub accounts /will have to create one during the ongoing lab (if not available already). Since provisioning of GitHub accounts for n number of users is not possible, the attendees are required to use their personal GitHub account. For ensuring account securities, we are using the “GitHub personal access token” so as the users don’t have to use their passwords while performing lab. The attendees can also delete the “GitHub personal access token” once they have performed the lab.
