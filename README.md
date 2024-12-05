FinalProject Setup Instructions

1. Preparing the Database

Notice:
Go to FinalProject\FinalProject\STOCK\bin\Debug and check for a file named connectdb.dba. If found, delete this file.

Step-by-Step Instructions:
Create Database in SQL Server:
Open Microsoft SQL Server Management Studio.
Create a new database named Product_Managerment.
Open the SQL file located at Final SE\final\Product_Managerment.sql and run it to populate the database.
2. Setting Up the Project in Visual Studio

Step 1: Open the Project
Open Visual Studio.
Load the solution file: FinalProject\FinalProject\FinalProject.sln.
Step 2: Update Data Model
In Solution Explorer, locate and delete the file STOCK.edmx in the STOCK folder.
Right-click the DataLayer folder → select Add → New Item.
Choose ADO.NET Entity Data Model and name it STOCK.
Step 3: Configure Database Connection
Click New Connection.
Enter your server name.
Select SQL Server Authentication and input your username and password.
Choose the database Product_Managerment → Click OK.
When prompted, select No, exclude sensitive data from the connection string.
Verify the connection string → Click Cancel to close without saving.
Click Next and select the tables, stored procedures, and functions.
Set the Model Namespace to STOCK → Click Finish.
Step 4: Save and Rebuild
Press Ctrl + S to save STOCK.edmx.
Rebuild the project: Build → Rebuild Solution.
Start the project to ensure it runs correctly.
3. Configuring Reports

Updating Report Data Sources
For ExportReport.rpt:

Double-click ExportReport.rpt.
Right-click → Select Database → Set Datasource Location.
Under Replace With, double-click OLE DB (ADO).
Choose Make New Connection → Select Microsoft OLE DB Provider for SQL Server.
Enter connection information (Database: Product_Managerment) → Finish.
Click the created database → Update.
For ReportPurchaseEntry.rpt:

Repeat the same steps as above for ReportPurchaseEntry.rpt.
Crystal Reports:
If Crystal Reports is not installed, download it from this link.

WebProject Setup Instructions

1. Initial Setup

Notice:
Open WebProject.sln.
Locate Web.config, find the <connectionStrings> section, and delete the existing connection string:
<add name="Product_ManagermentEntities" connectionString="..." />
2. Update Data Model

Step-by-Step Instructions:
Find and delete the file ProductEntities.edmx in the dbEntities folder.
Right-click the dbEntities folder → Add → New Item.
Choose ADO.NET Entity Data Model and name it ProductEntities.
Click New Connection and configure:
Enter server name and credentials.
Select the database Product_Managerment → Click OK.
Choose Yes, include sensitive data in the connection string.
Verify the connection string → Click Next.
Select tables, stored procedures, and functions.
Set Model Namespace to ProductEntities → Click Finish.
3. Save and Rebuild

Press Ctrl + S to save ProductEntities.edmx.
Rebuild the project: Build → Rebuild Solution.
Start the project and wait for the website to load at localhost:44308.
Demo and Support

Video Demo: YouTube Link
Login Credentials for Web:
User: admin@gmail.com
Password: 999999999
