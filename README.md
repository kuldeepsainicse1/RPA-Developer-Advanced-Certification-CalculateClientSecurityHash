# RPA-Developer-Advanced-Certification-CalculateClientSecurityHash

In this Certification for RPA Developer Advanced, you will create a UiPath automation that performs the steps below. 

To achieve this, you will use the REFrameWork as the starting template and follow the UiPath development best practices.

The solution has to be scalable, so create two separate projects (sub-processes):

One for the Dispatcher (add to queue);
Another one for the Performer (consume queue). 
Make sure you use a connection to an UiPath Orchestrator for testing.
Create Queue and update the name in Config.xlsx and Create ACME_Cred as Asset in Orchestrator with your username and password for ACME access.


Here are the steps performed by the Robot in the Dispatcher:

Log in to https://www.acme-test.com
On the landing page, Check for Dashboard, click Work Items menu. crape the data from the table displayed and add data with type as WI5 in array of DataRow.
For each row in the DataRow, Add a queue item containing the WIID
Close ACME System 1.


Steps performed by the Robot in the Performer:

Log in to https://www.acme-test.com.
For each Queue Item:
Open the Details page of the selected activity to retrieve the Client Details as ClientID, ClientName and ClientCountry. 
Replace all the variables with the corresponding values. Use dashes between each item and the above
Open the SHA1 Online webpage - http://www.sha1-online.com, and provide the following input : ClientID-ClientName-ClientCountry. 
Retrieve the Client Security Hash value from the webpage. 
Go back to Work Item Details and open Update Work Item
Set the status to “Completed”. Add a comment with the obtained SecurityHash

Note: Navigation can be achieved in multiple ways by the robot - choose whichever you find best.
