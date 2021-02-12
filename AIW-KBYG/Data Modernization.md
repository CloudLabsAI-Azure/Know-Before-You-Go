# MIGRATING SQL DATABASE TO AZURE

## Known Issues and workarounds

1. #### IMPORTANT!! 

  - Whenever attendee is asked to provide value for SUFFIX, it should be replaced with value which can be found from the Environment Details page. Not providing the SUFFIX value will lead to **Deployment issues** while deploying new resources, **Connection issues:** while connecting to database using **Microsoft SQL Server Management Studio 17(SSMS)** and** while performing **Database Assessment and Database Migration**. 



1. #### Exercise2 Task4 Step5:

   - While creating the storage account, make sure attendee provide the values as follows: 

       - Resource group: select existing then provide name hands-on-lab-SUFFIX 
       - Storage account: select Create new then provide name as **shellstorageSUFFIX** 
       - file share: select Create new then provide name as **shellfileSUFFIX** then create storage 

   - Attendees can find the SUFFIX value from the Environment Details page. 

1. #### Exercise4 Task1 step4:

   - Here attendee needs to select available subnet for the app service, if the attendee is not able to select any subnet then attendee needs to follow the next instructions to create the subnet. while creating the subnet users' needs to make sure the subnet address space is not overlapping other subnet's address space 
