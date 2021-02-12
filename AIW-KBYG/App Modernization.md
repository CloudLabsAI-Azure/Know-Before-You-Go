# App Modernization

## Known Issues and workarounds 

1. #### Important!

  - Whenever attendee is asked to provide value for **UniqueID**, it should be replaced with value which can be found from the Environment Details page. Not providing the UniqueID value will lead to 
      - **Deployment issues** : while deploying new resources, 
      - **Connection issues** : while connecting to database using **Microsoft SQL Server Management Studio 17(SSMS)** and** while performing **Database Assessment and Database Migration**. 

1. #### Exercise 3 Task 4 Step4:

   - While running the command to assign permissions to your service principal to read Secrets from Key Vault, make sure to replace the following values.
   
      - your-key-vault-name : **contoso-kv-UniqueId** ( You can find the UniqueID value by navigating to **Environment Details** page then selecting **Azure Credentials** tab)
      - http://contoso-apps :  **application id** ( You can find the service principal details by navigating to **Environment Details** page then selecting **Service Principal** tab)

1. #### Exercise 4 Task 5 Step 8: 

   - If you get the below web page after publishing Contoso.WebApi project instead of 'Page cannot be found' error message. 
     
    Follow the below Stpes to resolve the issue
    
    1. In the Azure portal, navigate to your Key Vault resource by selecting the hands-on-lab-SUFFIX resource group, and then selecting the contoso-kv-UniqueId Key vault resource from the list of resources.
    
    2. On the Key Vault blade, select Access policies under Settings in the left-hand menu, and then select + Add Access Policy.
 
    3. On the Add Access Policy dialog, enter the following: 

        •	Configure from template (optional): Leave blank. 
        
        •	Key permissions: Leave set to 0 selected. 
        
        •	Secret permissions: Select this, and then choose Get and List, to give yourself rights to manage secrets. 
        
        •	Certificate permissions: Leave set to 0 selected. 
        
        •	Select principal: From the Environment Details Tab,  selecting **ServicePrincipal Details** tab and copy display name of Service Principal then paste in the search box and select it from the suggestions. Then choose Select.
        
        •	Authorized application: Leave set to None selected. 
 
 
       Click on **Add**. 
 
    4. At last, click on Save on the Access policies toolbar. 
 
    5. Return to VSTS 2019, and publish the app again. 
 
