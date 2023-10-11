# BillingSystem is an example ASP.NET MVC application that demonstrate the "code first" approach to working with databases using Entity Framework.
# Create the application:
File menu>New>Project>select ASP.NET Core Web App (Model-View-Controller)>Next>Project name "BillingSystem">Next>select Framework ".NET 7.0", select Authentication type "none" and Configure for HTTPS>Create.
# Create Model class "BillRecord":
Right-click on the “Models” folder>Add>New Item>select "Class" and name it "BillRecord.cs".
# Add the connection string to be able to connect to MariaDB server:
Navigate to the “appsettings.json” file in the Solution Explorer. 
In the connection string, you put the name of the database “billlingsysdb” even though it is not existing yet. 
Also enter the password of your own instead of the one provided in this example application.
# Add a few packages to the solution of the application to enable using EF. 
Right-click on the solution>Manage NuGet Packages for Solution>Browse Tab. Here, there are three important packages to search for and install:

