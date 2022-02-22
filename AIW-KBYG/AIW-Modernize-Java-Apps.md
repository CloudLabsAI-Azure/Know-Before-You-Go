# Azure Virtual Workshop: Modernize Java Apps

Instructor should make sure that the attendees follow the lab guide provided in the environment to perform the lab instead of lab guide from MCW repo. Because few instructions may differ from the provided lab guides in GitHub repos.

##### Lab Guide Preview URL: [Lab Guide Preview](https://experience.cloudlabs.ai/#/labguidepreview/b6b935d8-5b46-4da1-9c26-7c76701c5a3b)

### Common Issues and workarounds
- [Known issues in Lab Steps](#known-issues-in-the-lab-steps)
- [Copy paste issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/CopyPaste)
- [Lab VM connectivity issue](https://docs.cloudlabs.ai/Learner/Troubleshooting/RDP)

## Known Issues in the lab steps:

### 1. Exercise-2 Task-5 Step-5

* While trying to access the **Test Endpoint url**.

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/Azure-spring-cloud-1.png)

* If you get an **"503 Service Temporarily Unavailable"** error as shown below.

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/Azure-spring-cloud-2.png)

* Click on **assign endpoint** and wait until the endpoint has been assigned and **unassign** the endpoint soon after.

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/Azure-spring-cloud-3.png)

### 2. Exercise-5 Task-6 

  ```
  az spring-cloud app logs --name spring-cloud-microservice -f
  ```

* Running the above command might take some time. If you do not see any output, Press **Ctrl+c** to stop the command. Doing so will display the output.

### 3. Exercise-12 Task-5

* Please open a new instance of Git Bash and login again using **az login** before running the following commands.

```
cd all-cities-weather-service
./mvnw clean package -DskipTests
az spring-cloud app deploy -n all-cities-weather-service --jar-path target/demo-0.0.1-SNAPSHOT.jar
cd ..
```

### 6. Azure API issue: 

* Due to recent changes in Azure api's, azure API's are taking some additional time to fetch the details of the resources . The validation steps might fail initially for the lab, if you re-run the steps again after 30-45 minutes later then it will succeed if there will be no configuration related issue with lab steps you performed.
