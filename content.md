﻿
<!---
Version: 1.0 
-->
# Exercise 1: Creating an Azure SQL Databases Instance
## INTRODUCTION MESSAGE
In this exercise, you will:  
  
Create a SQL Server instance in Azure.  
Create a database in Azure.  
  
The main tasks for this exercise are as follows:  
Sign in to the Azure Portal.  
Create an Azure SQL database by using the Azure Portal.
## COMPLETION MESSAGE
Results: After completing this exercise, you will have created both servers and databases in the SQL Database service.
### Login as Student
Login as Student with a password of Pa$$w0rd.

#### :bulb: KNOWLEDGE
You can use the Commands menu and choose Ctrl\+Alt\+Delete then click Student and enter Pa$$w0rd and press Enter. You can also use the Command menu and choose Paste/Paste Password instead of typing the password manually.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/08b256f8.jpg
>* ShowAutomatically = No





### On the Start screen, click Internet Explorer
On the Start screen, click the Internet Explorer tile

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666394.jpg
>* ShowAutomatically = No





### Go to the new Azure Portal
Go to https://portal.azure.com. Enter the email address of your Microsoft account associated with your Azure subscription. Then enter the password for your Microsoft account. Check Keep me signed in. Click Sign In.

#### :bulb: KNOWLEDGE
Before starting this lab, you must have completed the lab in Module 2. All work in this lab is done within vm20532 created in the lab in Module 2. Start and Connect via Azure Portal.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666395.jpg
>* ShowAutomatically = No



#### :calling: COMMAND
```TypeText
https://portal.azure.com
```


### Browse Virtual Machines
In the navigation pane on the left side of the Azure Portal, click Virtual Machines.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666396.jpg
>* ShowAutomatically = No





### Start the VM
Click the vm20532 VM that was created in the lab in Module 2 for development. In the Overview blade, if the VM is stopped, click Start and wait for the VM to start up. This may take a few minutes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666397.jpg
>* ShowAutomatically = No





### Connect to the VM via RDP
When the vm20532 VM has started, click Connect.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666398.jpg
>* ShowAutomatically = No





### Allow pop-ups
If presented with a message box that shows a pop-up has been blocked, select Options for this site and choose Always Allow. Then click Connect again.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672198.jpg





### Click Open
When presented with the RDP download pop-up at the bottom of the screen, click Open.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672199.jpg





### In the Remote Desktop Connection dialog box:
In the Remote Desktop Connection dialog box, perform the following steps:  
a. Click Don’t ask me again for connections to this computer to prevent this dialog box from displaying again.  
b. Click Connect.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666399.jpg
>* ShowAutomatically = No





### In the Windows Security dialog box:
In the Windows Security dialog box, perform the following steps:  
a. For the User name dialog box, provide the value, Student.  
b. For the Password dialog box, provide the value, AzurePa$$w0rd.  
c. Click OK.

#### :bulb: KNOWLEDGE
Note: If you computer is on a domain, you may need to add a backslash before the username to "escape" the domain.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666400.jpg
>* ShowAutomatically = No





### In the Remote Desktop Connection dialog box:
In the Remote Desktop Connection dialog box, perform the following steps:  
a. Verify if the Remote certificate name matches the name of your virtual machine.  
b. Click Don’t ask me again for connections to this computer to prevent this dialog box from displaying again.  
c. Click Yes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666401.jpg
>* ShowAutomatically = No





### Minimize Server Manager
Server Manager will start automatically after 30 seconds. When it starts, minimize it.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666402.jpg
>* ShowAutomatically = No





### On the Start screen, open Internet Explorer
On the Start screen, click the Internet Explorer tile.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666403.jpg
>* ShowAutomatically = No





### Sign in to the Azure Portal
Sign in to the Azure Portal at https://portal.azure.com. If prompted to allow azure.com to use additional storage on this computer, choose Yes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666404.jpg
>* ShowAutomatically = No



#### :calling: COMMAND
```TypeText
https://portal.azure.com
```


### New SQL Database blade
At the top-left corner of the portal, click \+ New. In the New blade that displays, click Databases, and then SQL Database from Databases blade.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666406.jpg





### In the SQL Database blade:
In the SQL Database blade that displays, locate the Database name box and provide the value db20532. 
Click Pricing Tier.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666407.jpg





### Select the Basic option
In the Choose your pricing tier blade that displays, select the Basic tile.  
Click Apply to close the blade.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666408.jpg





### Perform the following:
Perform the following actions on the SQL Database blade:  
a. For Select source, ensure Blank Database is selected.  
b. Click Server.   
c. In the Server blade that displays, click Create a new server.  
d. In the New Server blade that displays, locate the Server Name box.  
e. In the Server Name box, type sv20532\[Your Name Here\].  
f. In the Server Admin Login box, type testuser.  
g. In the Password box, type TestPa$$w0rd.  
h. In the Confirm Password box, type TestPa$$w0rd.  
i. In the Location list, select the region that is closest to your location.  
j. In the New server blade, click Select.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666409.jpg





### Create the SQL database and server
In the SQL database blade, make sure the Resource Group section is set to Use existing and that your pre-existing Resource Group is selected. Click Create to create the SQL database and server. This may take a few minutes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666410.jpg





### Verify database created
In the navigation pane on the left side, select SQL Databases. Verify that the db20532 database was created and is Online on the new Server named sv20532\[your name here\]

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/672207.jpg






# Exercise 2: Using Entity Framework with Local SQL Server
## INTRODUCTION MESSAGE
In this exercise, you will:  
  
Test the web application with local SQL data.  
The main tasks for this exercise are as follows:  
  
Run the ASP.NET web application to view events from the local SQL database.
## COMPLETION MESSAGE
Results: This Data Generation console application creates some sample data in your local SQL database \)LocalDb) so that you can test the ASP.NET web application.
### Open an existing ASP.NET web application project
On the taskbar, click the File Explorer icon. In the Libraries window, go to Allfiles \)F):\\Mod04\\Labfiles\\Starter\\Contoso.Events, and then double-click Contoso.Events.sln.

#### :bulb: KNOWLEDGE
Note that Known file extensions \)such as .sln) may be hidden. See screenshot. It may also take a while for Visual Studio 2015 to open.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666411.jpg
>* ShowAutomatically = No





### Debug DataGeneration project
In the Solution Explorer pane, right-click the Contoso.Events.DataGeneration project, point to Debug, and then click Start New Instance. Wait for the data generation to complete.

#### :bulb: KNOWLEDGE
Note: The Data Generation script takes between one to two minutes to run.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666412.jpg
>* ShowAutomatically = No





### View Output
When the Data Generation has completed, click the Output tab to review the output. Verify it has finished with code 0.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666414.jpg





### Set Startup Project
In the Solution Explorer pane, scroll down then right-click the Contoso.Events.Web project, and then click Set as Startup Project.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666415.jpg





### On the Debug menu, click Start Debugging.
On the Debug menu, click Start Debugging.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666416.jpg





### Verify that it shows a list of multiple events
On the home page of the web application, verify that it shows a list of multiple events. Close the tab that is displaying the website.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666413.jpg
>* ShowAutomatically = No






# Exercise 3: Using Entity Framework with Azure SQL Databases
## INTRODUCTION MESSAGE
In this exercise, you will:  
  
Configure an Entity Framework Code First DatabaseInitializer.  
Implement a Seed method for the initializer.  
Publish a Web App application.  
View tables and data by using the Azure SQL Database Portal.  
  
The main tasks for this exercise are as follows:  
Configure DbContext with a new DatabaseInitializer.  
Implement seed data with DbContext.  
Publish the cloud application with updated DbContext to Azure.  
Verify that the Azure Web App website is using the new data.  
Sign in to the Azure Portal.  
View the migrated data in the Azure SQL Portal.
## COMPLETION MESSAGE
Results: After completing this exercise, you will have configured Entity Framework to initialize a new database with seed data.
### Add New Item to project
In the Solution Explorer pane, right-click the Contoso.Events.Data project, point to Add and then click New Item.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666425.jpg





### In the Add New Item dialog box, perform:
In the Add New Item dialog box, perform the following steps:  
a. Expand Installed, expand Visual C\# Items, and then click Code.  
b. Click the Class template.  
c. In the Name box, type EventsContextInitializer.cs.  
d. Click Add.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666426.jpg





### Add a using statements at the top:
Add this using statement at the top of the code file:  
using System.Data.Entity;

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666429.jpg



#### :calling: COMMAND
```TypeText
using System.Data.Entity;
```


### Add the public accessor
In the EventsContextInitializer class, add the public accessor to the left of the class definition:  
class EventsContextInitializer  
Verify that the updated class definition looks like the following line of code:  
public class EventsContextInitializer

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666427.jpg





### Add the CreateDatabaseIfNotExists statement
In the EventsContextInitializer class, add the CreateDatabaseIfNotExists<EventsContext> inheritance statement to the right of the class definition:  
public class EventsContextInitializer  
Verify that the updated class definition looks like the following line of code:  
public class EventsContextInitializer : CreateDatabaseIfNotExists<EventsContext>

#### :bulb: KNOWLEDGE
You can Auto Hide the Solution Explorer by clicking the push-pull pin on the window.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666428.jpg



#### :calling: COMMAND
```TypeText
public class EventsContextInitializer : CreateDatabaseIfNotExists<EventsContext>
```


### Open the EventsContext.cs file.
In the Solution Explorer pane, expand the Contoso.Events.Data project. In the Contoso.Events.Data project, open the EventsContext.cs file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666430.jpg





### Modify the static constructor:
Within the static constructor static EventsContext\)), add the following line of code:  
Database.SetInitializer<EventsContext>\)new EventsContextInitializer\)));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666431.jpg



#### :calling: COMMAND
```TypeText
            Database.SetInitializer<EventsContext>(new EventsContextInitializer());
```


### Save the EventsContext.cs file.
Save the EventsContext.cs file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666432.jpg





### Open the EventsContextInitializer.cs file.
In the Solution Explorer pane, expand the Contoso.Events.Data project. In the Contoso.Events.Data project, open the EventsContextInitializer.cs file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666433.jpg





### Add the following method declaration:
Add the following method declaration to the EventsContextInitializer class:  
protected override void Seed\)EventsContext context)\{ \}

#### :bulb: KNOWLEDGE
Note that the editor will convert the code \{ \} to a standard format:  
\{   
base.Seed\)context);EventsContext context) \{ \}  
\}  
  
This will be overwritten in a later step.  
Ignore Intellisense errors. These will be corrected later.  
 \)see screenshot)

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666434.jpg



#### :calling: COMMAND
```TypeText
protected override void Seed(EventsContext context){ }
```


### Add the following using statement:
Add the following using statement at the top of the code file:  
using Contoso.Events.Models;

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666435.jpg



#### :calling: COMMAND
```TypeText
using Contoso.Events.Models;
```


### Modify the Seed(EventsContext context) method
Place the cursor before the closing brace of the Seed\)EventsContext context) method, and then type the following lines of code replacing the existing line of code:  
if \)context.Events.Count\)) == 0)  
 \{  
     Event eventItem = new Event\));  
     eventItem.EventKey = "FY17SepGeneralConference";  
     eventItem.StartTime = DateTime.Today;  
     eventItem.EndTime = DateTime.Today.AddDays\)3d);  
     eventItem.Title = "FY17 September Technical Conference";  
     eventItem.Description = "Sed in euismod mi.";  
     eventItem.RegistrationCount = 1;  
     context.Events.Add\)eventItem);  
 \}

#### :bulb: KNOWLEDGE
Overwrite the code:  
base.Seed\)context);EventsContext context) \{ \}  
  
Note: If you use the "A" button \)type text) you will need to add your own carriage-return line-feed \)CRLF) characters.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666436.jpg



#### :calling: COMMAND
```TypeText
if (context.Events.Count() == 0)
 {
     Event eventItem = new Event();
     eventItem.EventKey = "FY17SepGeneralConference";
     eventItem.StartTime = DateTime.Today;
     eventItem.EndTime = DateTime.Today.AddDays(3d);
     eventItem.Title = "FY17 September Technical Conference";
     eventItem.Description = "Sed in euismod mi.";
     eventItem.RegistrationCount = 1;
     context.Events.Add(eventItem);
 }
```


### Add to the Seed(EventsContext context) method
Place the cursor before the closing brace of the Seed\)EventsContext context) method, and then type the following lines of code:  
if \)context.Registrations.Count\)) == 0)  
 \{  
     Registration registrationItem = new Registration\));  
     registrationItem.EventKey = "FY17SepGeneralConference";  
     registrationItem.FirstName = "Aisha";  
     registrationItem.LastName = "Witt";  
     context.Registrations.Add\)registrationItem);  
 \}

#### :bulb: KNOWLEDGE
Note: If you use the "A" button \)type text) you will need to add your own carriage-return line-feed \)CRLF) characters.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666437.jpg



#### :calling: COMMAND
```TypeText
if (context.Registrations.Count() == 0)
 {
     Registration registrationItem = new Registration();
     registrationItem.EventKey = "FY17SepGeneralConference";
     registrationItem.FirstName = "Aisha";
     registrationItem.LastName = "Witt";
     context.Registrations.Add(registrationItem);
 }
```


### Add code to Seed(EventsContext context) method
Place the cursor before the closing brace of the Seed\)EventsContext context) method, and then type the following line of code:  
context.SaveChanges\));

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666438.jpg



#### :calling: COMMAND
```TypeText
context.SaveChanges();
```


### Save the EventsContextInitializer.cs file.
Save the EventsContextInitializer.cs file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666439.jpg





### Build Project
In the Solution Explorer pane, right-click the Contoso.Events.Data project, and then click Build.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666440.jpg





### Review Output
Verify Build succeeded

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666441.jpg





### Open the Web.Release.config file.
In the Solution Explorer pane, expand the Contoso.Events.Web project. Expand the Web.config file in the Contoso.Events.Web project. Double-click the Web.Release.config file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666442.jpg





### Update the Web.Release.config file
In the Web.Release.config file, update the connection string using the key EventsContextConnectionString with the following values:  
\[database\]: db20532  
\[login\]: testuser  
\[server\]: sv20532\[Your Name Here\]. \)Note that there are two different places to replace \[server\].)  
\[password\]: TestPa$$w0rd

#### :warning: ALERT
Note: Ensure that you remove the square brackets as you replace each placeholder.

#### :bulb: KNOWLEDGE
The word wrap feature will cause a visual glyph \)line break) in the middle of the password. This is actually OK. To verify, you can switch off the word wrap feature in Tools/Options/Text Editor/All Languages.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666443.jpg





### Save the Web.Release.config file.
Save the Web.Release.config file.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666444.jpg





### Publish Project
In the Solution Explorer pane, right-click the Contoso.Events.Web project, and then click Publish.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666445.jpg





### Select Microsoft Azure App Service
In the Publish Web window, click Microsoft Azure App Service.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666446.jpg





### In the App Service dialog, perform the following:
In the App Service dialog, perform the following steps:  
a. Select your Azure subscription.  
b. Ensure that the Resource Group option is selected in the View list.  
c. Click the New button.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666447.jpg





### In the Create App Service dialog, perform:
In the Create App Service dialog, perform the following steps:  
a. Ensure that you have an auto-generated Web App name. If not, enter a globally unique name.  
b. Select your Azure subscription.  
c. In the Resource Group dialog box, verify that your pre-existing Resource Group is specified.  
d. Click the New button immediately to the right of the App Service Plan dialog box.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666448.jpg





### In the App Service Plan form:
f. Ensure that you have an auto-generated App Service Plan name. If not, provide the value TestSQLPlan.  
g. In the Location list, select the region that is closest to your location. Ensure that this region is same as the region where you created SQL Database.  
h. In the Size list, select the Free option.  
i. Click the OK button to close the Configure App Service Plan dialog.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666449.jpg





### Create your App Service instance
j. Click the Create button to create your App Service instance.  
           

#### :bulb: KNOWLEDGE
Note: The deployment process for the new App Service is relatively short and should take 2-5 minutes.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666450.jpg





### Click Publish
In the Publish Web dialog box, perform the following steps:  
a. Leave the default values in all the fields.  
Click Publish

#### :bulb: KNOWLEDGE
Note: It typically takes a minute for the publish process to complete. You can track the progress of your publish in the Web Publish Activity \)View > Other Windows > Web Publish Activity ) pane that displays when you publish your Web App project. You can aslo view the Output pane.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666451.jpg





### Wait for the publish process to complete
Wait for the publish process to complete \)the web page will open). Click on the Visual Studio icon on the task bar to switch back and view the Output window to display the message Succeeded.

#### :bulb: KNOWLEDGE
Note: The publish process is complete when the message “Succeeded” displays in the Web Publish Activity pane. The green circular indicator in the Web Publish Activity pane does not indicate that the publish process is complete, but it indicates that the package is uploaded successfully.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666452.jpg





### In the Web Publish Activity pane:
In the Web Publish Activity pane, click the hyperlink that directs you to the published web application. The same hyperlink is in the Output window also.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666453.jpg





### Verify that the website displays the single event
Verify that the website displays the single event that you created in your Entity Framework context initializer. Close the tab.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666454.jpg





### Switch back to the Azure Portal
Switch back to the Azure Portal. It should still be open in another tab. If not, open https://portal.azure.com and login, if necessary.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666455.jpg





### Browse SQL databases
In the Browse blade, click SQL databases. In the list of SQL Databases, select the SQL database named db20532.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666456.jpg





### In the db20532 - SQL database Overview blade:
In the db20532 - SQL database Overview blade, locate the Essentials panel. Locate the Server name section and click on the associated hyperlink to navigate to the server blade.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666457.jpg





### In the SQL server blade, show firewall settings
In the SQL server Overview blade, locate the Essentials panel. Locate the Firewall section and click on the associated hyperlink to navigate to Show firewall settings.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666458.jpg





### Add client IP to firewall settings
In the Firewall settings blade, click the Add client IP button to add your virtual machine's IP Address to the list of allowed IP Address ranges.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666459.jpg





### Click on Save at the top of the blade.
Click on Save at the top of the blade. Once saved, close the confirmation dialog by clicking the Ok button.

#### :bulb: KNOWLEDGE
Note: It might take a minute for the firewall changes to get updated on server.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666460.jpg





### Switch to Visual Studio Server Explorer
Return to the open instance of Visual Studio. In Visual Studio, open the View menu and then select the Server Explorer option.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666461.jpg





### In Server Explorer, add connection
Expand the Data Connections node. Right click on Data Connections and click on Add Connection.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666462.jpg





### Choose Microsoft SQL Server for data source
Choose Microsoft SQL Server for data source and click Continue

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666463.jpg





### In the Add Connection window
In the Add Connection wizard, provide following values and click OK.  
a. In the server name box, type sv20532\[your name\].database.windows.net.  
b. Select Use SQL Server Authentication.  
c. In the Username box, type testuser.  
d. In the Password box, type TestPa$$w0rd.  
e. In the Select or enter a database name dropdown, select db20532.  
f. Click the OK button.

#### :bulb: KNOWLEDGE
Note: If firewall rules are not updated on the server, you may have to wait a few more minutes before proceeding.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666464.jpg





### View Tables in Server Explorer
On Visual Studio Server Explorer, expand Data Connections then sv20532\[your name\].db20532.dbo and then the Tables node. Right click Tables and click Refresh

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666465.jpg





### In the dbo.Events table, view the single record.
Right click Events table, and then select Show Table Data. In the dbo.Events table, view the single record.

#### :bulb: KNOWLEDGE
Note: If an error results, try closing and reopening Visual Studio.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666466.jpg





### Close Visual Studio 2015
Close Visual Studio 2015

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666418.jpg
>* ShowAutomatically = No





### Close Internet Explorer
Close Internet Explorer

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666417.jpg
>* ShowAutomatically = No





### Close File Explorer
Close File Explorer

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666419.jpg
>* ShowAutomatically = No





### Close Server Manager
Close Server Manager

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666420.jpg
>* ShowAutomatically = No





### Close RDP session
Close RDP session and click OK to disconnect

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666421.jpg
>* ShowAutomatically = No





### Stop VM to save billing charges
If you are stopping labs for the day, on the vm2032 Overview page in the Azure Portal, click Stop to stop billing charges until you start labs again. When prompted, click Yes to stop the VM.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666422.jpg
>* ShowAutomatically = No





### Close Internet Explorer
Close Internet Explorer to end the lab

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/666423.jpg
>* ShowAutomatically = No






