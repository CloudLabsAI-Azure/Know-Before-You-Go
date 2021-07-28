# App Modernization

## Known Issues and workarounds 

- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)
- [Lab Known Issues](#issue-related-to-azure-migrate-gui-in-exercise-2-and-exercise-3)

### Issue related to Azure Migrate GUI in Exercise 2 and Exercise 3: 

1. **In Exercise 2: Task 2: Migrate the web application to Azure App Service : Step 7**

  - After completing the migration of the app service, The discovered web servers, assessed websites and migrated websites are **not visible** from the Portal on **Azure migrate.** This is an issue in Azure Migrate GUI and we have engagged MS support team on this and we don't have any ETA on this from MS support team.

  - The **web servers** are **discovered** and website is **assessed** in actual and you can **proceed** with the next steps. This is a **GUI issue** and **won't affect any functionality.**

    ![](https://raw.githubusercontent.com/junnhssn/Know-Before-You-Go/main/media/app-mod-azure-migrate-1.png)

2. **In Exercise 3 : Task 1: Perform assessment for migration to Azure SQL Database : Step 14**

  - After uploading the **PartsUnlimited** database assessment to Azure. The changes are **not visible** from the Portal on **Azure Migrate.**
  
  - This is also a **GUI issue** and **won't affect any functionality** and you can proceed with the next steps.

     ![](https://raw.githubusercontent.com/junnhssn/Know-Before-You-Go/main/media/app-mod-azure-migrate-2.png)
