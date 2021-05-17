# Azure Spring Cloud 

## Known Issues and workarounds 

### 1. Exercise 2, Task 5 Step 5

* While trying to access the **Test Endpoint url**.

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/Azure-spring-cloud-1.png)

* If you get an **"503 Service Temporarily Unavailable"** error as shown below.

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/Azure-spring-cloud-2.png)

* Click on **assign endpoint** and wait until the endpoint has been assigned and **unassign** the endpoint soon after.

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/Azure-spring-cloud-3.png)

### 2. Exercise 5 Task 6 

```
az spring-cloud app logs --name spring-cloud-microservice -f
```


* Running the above command might take some time. If you do not see any output, Press **Ctrl+c** to stop the command. Doing so will display the output.



### 3. Exercise 12 Task 5

* Please open a new instance of Git Bash and login again using **az login** before running the following commands.

```
cd all-cities-weather-service
./mvnw clean package -DskipTests
az spring-cloud app deploy -n all-cities-weather-service --jar-path target/demo-0.0.1-SNAPSHOT.jar
cd ..
```

### 4. If Copy paste doesn’t work, please try following: 

* Please check if Clipboard permissions are on **Allow**, if not then change it to **Allow**.

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-1.png)

* After allowing the clipboard content if you are not able to Copy the Content from lab Guide into the VM using copy button, then select the content which you want to copy from lab guide then right click > Copy to copy the content and then try to paste at desired location in Lab VM.

* Try to refresh the page or try any other Web Browser. 

* Check on Network bandwidth in your local System/Laptop. 

If the above points don’t work, then directly connect to the Lab VM using Remote Desktop Connection using the **Credentials** provided in **Environment Details** page.  

* Copy the **LabVM/JumpVM DNS Name, Username** and **Password** from **Environment details** page 

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-2.png)

* Search for **Remote Desktop Connection** App from Start Menu items of your local Laptop/Desktop and then select the **Remote Desktop Connection** App. 

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-3.png)

* Paste the **VM DNS Name** in Computer field and then, click on **Connect**. 

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-4.png)

* Click on **More choices**.  

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-5.png)

* Now, click on the **Use a different account**.

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-6.png)

* Now, enter the **VM Admin username** and **password** which you have copied from Environment details page and click on **Ok** button. Please add dot and back-slash **“.\”** before the Admin username.  

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-7.png)

* Next, click on the **Yes** button to accept the certificate and add in trusted certificates.  

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-8.png)

* If **LabVM** opens on full screen, then you can **Restore Down** the window.  

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-9.png)

* Split the Window from lab environment page to open the Lab guide in Separate Window. 

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-10.png)

* Now, copy the lab environment URL from the list and open that inside the VM itself and then use the Vm on full screen. 

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-11.png)


### 5. If RDP over HTTP doesn’t work, please try following:

* Please check if the cookies are enabled or not in your browser, if not then please **Enable**.

*	Check if your browser is updated to **latest version** and if you are still facing the issue then please try in the different Browser.

*	Try to open the Lab Environment in **Private/Incognito** Window.

*	Try to Restart the VM from the Lab Environment Page.

![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/RDPoverHTTP%201.png)

* If the above points don’t work, then directly connect to the Lab VM using Remote Desktop Connection using the **Credentials** provided in **Environment Details** page.  


