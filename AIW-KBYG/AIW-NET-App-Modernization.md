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
   
        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/appmodissue1.png?raw=true)
     
    Follow the below Stpes to resolve the issue
    
    1. In the Azure portal, navigate to your Key Vault resource by selecting the hands-on-lab-SUFFIX resource group, and then selecting the contoso-kv-UniqueId Key vault resource from the list of resources.
    
         ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/appmodissue2.png?raw=true)
            
    2. On the Key Vault blade, select Access policies under Settings in the left-hand menu, and then select + Add Access Policy.
    
        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/appmodissue3.png?raw=true)
 
    3. On the Add Access Policy dialog, enter the following: 

        •	Configure from template (optional): Leave blank. 
        
        •	Key permissions: Leave set to 0 selected. 
        
        •	Secret permissions: Select this, and then choose Get and List, to give yourself rights to manage secrets. 
        
         ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/appmodissue4.png?raw=true)
        
        •	Certificate permissions: Leave set to 0 selected. 
        
        •	Select principal: From the **Environment Details** Tab,  selecting **ServicePrincipal Details** tab and copy **Display name** of Service Principal then paste in the search box and select it from the suggestions. Then choose **Select**.
        
          ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/appmodissue6.png?raw=true)
                
          ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/appmodissue5.png?raw=true)
                        
        
        •	Authorized application: Leave set to None selected. 
 
 
       Click on **Add**. 
       
         ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/appmodissue7.png?raw=true)
 
    4. At last, click on **Save** on the Access policies toolbar. 
 
    5. Return to VSTS 2019, and publish the app again. 

1. **Copy-Paste Issue**

    **If Copy paste doesn’t work, please try following:** 

      - Please check if Clipboard permissions are on **Allow**, if not then change it to **Allow**. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-1.png?raw=true) 

      - After allowing the clipboard content if you are not able to Copy the Content from lab Guide into the VM using copy button, then select the content which you want to copy from lab guide then right click > Copy to copy the content and then try to paste at desired location in Lab VM. 
      
      - Try to refresh the page or try any other Web Browser. 
      
      - Check on Network bandwidth in your local System/Laptop. 

     If the above points don’t work, then directly connect to the Lab VM using Remote Desktop Connection using the **Credentials** provided in **Environment Details** page.  

      - Copy the **LabVM/JumpVM DNS Name, Username** and **Password** from **Environment details** page 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-2.png?raw=true) 

      - Search for **Remote Desktop Connection** App from Start Menu items and then select the **Remote Desktop Connection** App. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-3.png?raw=true) 

      - Paste the **VM** **DNS Name** in Computer field and then, click on **Connect**. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-4.png?raw=true) 

      - Click on **More choices**. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-5.png?raw=true) 

      - Now, click on the **Use a different account.** 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-6.png?raw=true) 

      - Now, enter the **VM Admin username** and **password** which you have copied from Environment details page and click on **Ok** button. Please add dot and back-slash “**.\”** before the Admin username. 

         ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-7.png?raw=true) 

      - Next, click on the **Yes** button to accept the certificate and add in trusted certificates. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-8.png?raw=true) 

      - If **LabVM** opens on full screen, then you can **Restore Down** the window. 

        ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-9.png?raw=true) 

      - Split the Window from lab environment page to open the Lab guide in Separate Window. 

          ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-10.png?raw=true) 

      - Now, copy the lab environment URL from the list and open that inside the VM itself and then use the Vm on full screen. 

          ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-11.png?raw=true) 
 
