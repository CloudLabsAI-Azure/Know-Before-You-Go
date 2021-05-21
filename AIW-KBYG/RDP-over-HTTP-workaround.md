# Remote Desktop Functionality Known Issues :

 If RDP over HTTP fuctionality doesn’t work while accessing the lab environment, request you to please try following:

* Check if the cookies are enabled in your browser, if not then please **Enable**.

# Steps to Enable Cookies in the Browsers

* If you are using Safari browser, then please follow the below steps :

->  Click the Safari menu from the top toolbar.
->  Choose Preferences.
->  Click the Privacy tab.
->  Click the Never checkbox for Block Cookies.

* If you are using Chrome browser, then please follow the below steps : 

-> Click the context menu in the browser toolbar to the right of the address bar.
-> Choose Settings.
-> Click "Show Advanced Settings."
-> Click Content settings in the Privacy section.
-> Ensure that the bullet for "Allow local data to be set (recommended)" is checked.
-> Also ensure that "Block third-party cookies and site data" is unchecked.

* If you are using Firefox broser, then please follow the below steps: 

-> Click the Tools menu from the top toolbar.
-> Choose Options.
-> Click the Privacy tab.
-> Under "History" select "Use custom settings for history" from the drop-down menu beside "Firefox will."
-> Ensure that the checkboxes for "Accept cookies from sites" and "Accept third-party cookies" are both checked.
-> Click OK.

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
  
# Contact Support:

In case of any issue, you can reach us on Live Chat support: https://cloudlabs.ai/microsoft-support and also can drop us an email on cloudlabs-support@spektrasystems.com

