# Remote Desktop Functionality Known Issues :





#### Sometime, JumpBox/LabVM RDP Connection (RDP Gateway connection) doesn't work at customers/attendee's network due to following reasons :
  * Organization firewall/policy blocking the connection.
  * User is connected to any VPN (Virtual Private Network), which may restrict the connection based on network policies.
  * There may be cookies and cache problem in internet browser.
  * Low network bandwidth (Network bandwidth recommended: 8 Mbps).



#### It can be fixed by trying the following steps:
  * Make sure you are connected with good internet connection with minimum network bandwidth 8 Mbps.
  * Try to clear cache from the browser, [Enable Cookies](#steps-to-enable-cookies-in-the-browsers). 
  * Try to launch the lab in **Private/Incognito** browsing mode.
  * If all the above steps won't work, then try to connect VM using [Remote Desktop Connection](#connect-vm-using-remote-desktop-connection-from-your-system) in your Computer/Laptop. Jump Box/LabVM **credentials** are provided on lab **Environment Details** page. Steps are documented [here](#connect-vm-using-remote-desktop-connection-from-your-system) to connect to JumpBOX/LabVM using Remote Desktop Connection. 
  * If the above step doesn't work check with Network Administrator of your organization if that specific traffic is getting blocked or have any restrictions.
  * Try to Restart the VM from the Lab Environment Page (as shown in the image below).

   ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/RDPoverHTTP%201.png)
  


### Connect VM using Remote Desktop Connection from your System

* Copy the **LabVM/JumpVM DNS Name, Username** and **Password** from **Environment Details** page 

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-2.png)

* Search for **Remote Desktop Connection** Application from Start Menu of your local Laptop/Desktop and then select the **Remote Desktop Connection** Application (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-3.png)

* Paste the **VM DNS Name** in Computer field and then, click on **Connect** (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-4.png)

* Click on **More choices** (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-5.png)

* Now, click on the **Use a different account** (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-6.png)

* Now, enter the **VM Admin username** and **password** which you have copied from Environment details page and click on **Ok** button. Please add a dot followed by a back-slash **“.\”** before the Admin username (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-7.png)

* Next, click on the **Yes** button to accept the certificate and add in trusted certificates (as mentioned in the image below).

  ![](https://github.com/CloudLabsAI-Azure/Know-Before-You-Go/blob/main/Labs/images/copypasteissue-8.png)
  


### Steps to Enable Cookies in the Browsers

#### If you are using Safari browser, then please follow the below steps:

-> Click the Safari menu from the top toolbar.
-> Choose Preferences.
-> Click the Privacy tab.
-> Click the Never checkbox for Block Cookies.

#### If you are using Chrome browser, then please follow the below steps : 

-> Click the context menu in the browser toolbar to the right of the address bar.
-> At the top right, click More Moreand then Settings.
-> Under "Privacy and security," click Site settings.
-> Click Cookies.
-> From here, you can:
-> Turn on cookies: Next to "Blocked," turn on the switch.
-> Turn off cookies: Turn off Allow sites to save and read cookie data.

#### If you are using Firefox browser, then please follow the below steps: 


In the Menu bar at the top of the screen, click Firefox and select Preferences.
-> Click the menu button and select Options.
-> Select the Privacy & Security panel. 
-> To allow cookies, make sure that the Check-Box for "Cookies" is unchecked.
-> Close the page. Any changes you've made will automatically be saved.
  
# Contact Support:

In case of any issue, you can reach out to us Live Chat support: https://cloudlabs.ai/microsoft-support and also can drop us an email on cloudlabs-support@spektrasystems.com

