# Remote Desktop Functionality Known Issues :

 If RDP over HTTP fuctionality doesn’t work while accessing the lab environment, request you to please try following:

* Check if the cookies are enabled in your browser, if not then please **Enable**.

*	Check if your browser is updated to **latest version** and if you are still facing the issue then please try in a different Browser.

*	Try to access the Lab Environment in **Private/Incognito** Window. 

*	Try to Restart the VM from the Lab Environment Page (as mentioned in the image below).
  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/RDPoverHTTP%201.png)

* If the above actions did not work, you can then directly connect to the Lab VM using Remote Desktop Connection using the **Credentials** provided in **Environment Details** page (as mentioned in the image below).

   * Copy the **LabVM/JumpVM DNS Name, Username** and **Password** from **Environment details** page 

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-2.png)

* Search for **Remote Desktop Connection** Application from Start Menu of your local Laptop/Desktop and then select the **Remote Desktop Connection** Application (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-3.png)

* Paste the **VM DNS Name** in Computer field and then, click on **Connect** (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-4.png)

* Click on **More choices** (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-5.png)

* Now, click on the **Use a different account** (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-6.png)

* Now, enter the **VM Admin username** and **password** which you have copied from Environment details page and click on **Ok** button. Please add dot and back-slash **“.\”** before the Admin username (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-7.png)

* Next, click on the **Yes** button to accept the certificate and add in trusted certificates (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-8.png)
