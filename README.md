# BillingSystem is an example ASP.NET MVC application that demonstrate the "code first" approach to working with databases using Entity Framework.
# Create the application:
File menu>New>Project>select ASP.NET Core Web App (Model-View-Controller)>Next>Project name "BillingSystem">Next>select Framework ".NET 7.0", select Authentication type "none" and Configure for HTTPS>Create.
# Create Model class "BillRecord":
Right-click on the "Models" folder>Add>New Item>select "Class" and name it "BillRecord.cs".
# Add the connection string to be able to connect to MariaDB server:
Navigate to the "appsettings.json" file in the Solution Explorer. 
In the connection string, you put the name of the database "billlingsysdb" even though it is not existing yet. 
Also enter the password of your own instead of the one provided in this example application.
# Add a few packages to the solution of the application to enable using EF and handle the connection to the database. 
Right-click on the solution>Manage NuGet Packages for Solution>Browse Tab. 
Here, there are three important packages to search for and install: "Microsoft.EntityFrameworkCore", "Microsoft.EntityFrameworkCore.Design", "Microsoft.EntityFrameworkCore.Tools", and "Pomelo.EntityFrameworkCore.MySql".
# Create the class “BillingContext" as derived from DbContext class:
Right-click on the "Models" folder>Add>New Item> nane it "BillingContext.cs". 
The class is derived from DbContext class, which is a primary class in EF Core functionality for interacting with the database in an object-oriented manner without having to write raw SQL queries.
The "DbSet" represents a collection of all the "BillRecord" entities in the database, essentially representing the "BillRecords" table in the database. 
Through this property "DbSet", you can perform operations like querying the table, adding new records, or deleting existing ones.
# Create another view and call it “Records” to display the inserted records. 
# Create a new controller "BillingController":
Right-click on “Controllers” folder>Add>Controller>name it "BillingController.cs".
This controller will interact with the “BillingContext” to insert and display data.
# Create folder “Billing” under “Views”. 
# Create new views in the created "Billing" folder.
Right-click on the "Billing" folder>Add>View>select "Razor View - Empty">name it "Index.cshtml" and call the model "BillRecord" in it.
Then set the layout of the form to use for inserting data into the database.
Create another view and call it "Records" to display the inserted records.
# Now, before you run the application, there are two important commands you need to run in the “Package Manager Console”:
Go to Tools menu in Visual Studio>NuGet Package Manager>Package Manager Console.
Type the following commands to create the "billingsysdb" database and "billrecords" table:
1- Add-Migration InitialCreate (Then press Enter)

2- o	Update-Database (Then press Enter)


