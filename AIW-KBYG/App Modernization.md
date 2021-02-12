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
