# Azure Virtual Workshop: Cloud Adoption Framework

In this lab all the exercises are independent to each other.

## Known Issues and workarounds 
1. [Jumpbox/LabVM connectivity/RDP over HTTP issue](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/AIW-KBYG/RDP-over-HTTP-Workaround.md#remote-desktop-functionality-known-issues-)

2. **Increased time with ARM template deployment:** As compared to the older version of the lab – The ARM template deployment time has been increased and it is mentioned in the lab guide instructions that the deployment of ARM template can take up to 90 minutes as it consists of resources which take time to deploy hence it is expected. 

3. In Exercise 1 Task 1 and step 16, ARM template deployments fails sometime. Deployment fails with policy assignments, sometime private DNS endpoint deployment fails. This is a known issue you potentially can run into as described here: https://github.com/Azure/Enterprise-Scale/blob/main/docs/EnterpriseScale-Known-Issues.md#deploying-the-reference-implementation-fails-due-to-policy--cannot-be-found-404

   **Fix deployment**: 
     * Redeploy the template by following the Exercise 1 Task 1
     * If redeploying the template fails again, then cleanup the management groups, policy assignments and resource groups which got deployed as part of ARM tremplate deployment in exercise 1 and task 1. Now, deploy the template again.

4. **Usage of personal GitHub accounts:**
     The attendees will need to have their own GitHub accounts /will have to create one during the ongoing lab ( if not available already). Since provisioning of GitHub accounts for n number of users is not possible, the attendees are required to use their personal GitHub account. For ensuring account securities, we are using the “GitHub personal access token” so as the users don’t have to use their passwords while performing lab. The attendees can also delete the “GitHub personal access token” once they have performed the lab.
