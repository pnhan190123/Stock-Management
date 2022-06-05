Instruction to open source FinalProject and link database to source
*Notice: go to FinalProject\FinalProject\STOCK\bin\Debug
Check if it have a file name connectdb.dba -> delete this file.

Step 1: Create database name as file (Product_Managerment) database in Microsoft SQL Server Management Studio then open file name in Final SE\final\Product_Manangerment.sql to database name (Product_Managerment)
Step 2: Open Visual Studio with the link FinalProject\FinalProject\FinalProject.sln
Step 3: Find the file name STOCK.edmx in STOCK in Solution Exporer and delete it 
Step 4: Find the file DataLayer press the right click in mouse -> click to Add -> create new file -> search the ADO.NET Enity Data Model and set name is STOCK
-> Next -> press New Connection -> add your sever name -> choose Authentication: SQL Sever Authentication 
-> Enter your username and password -> in connect to a database click select or enter a database name: Product_Managerment -> OK
-> After click OK the hud will back to Entity Data Model Wizard 
-> Click No, exclude sensitive data from the connection string -> Remember to check Connection string carefully -> Then cancle click in save
-> Next
-> Click choose Tables and Stored Procedures and Functions -> Set Model Namespace is STOCK -> Finish
Step 5: Ctrl + S in file name STOCK.edmx
Step 6: Rebuild - Start 
Step 7: To print data -> Find file name ExportReport.rpt and ReportPurchaseEntry.rpt
*ExportReport.rpt-> double click -> press right mouse choose Database -> choose set datasource location -> look below in Replace with -> double click OLE DB(ADO)
-> choose Make new connection -> choose Microsoft OLE DB Provider for SQL Sever -> Next -> Fill your connection information (Notice Database: Product_Manangerment) -> Finish
-> Click database was created -> Click update
*ReportPurchaseEntry.rpt-> double click -> press right mouse choose Database -> choose set datasource location -> look below in Replace with -> double click OLE DB(ADO)
-> choose Make new connection -> choose Microsoft OLE DB Provider for SQL Sever -> Next -> Fill your connection information (Notice Database: Product_Manangerment) -> Finish
-> Click database was created -> Click update
*If your computer don't have Crystal Report you can download here https://drive.google.com/file/d/1884fQ2pSQm2iGGuRo5RCokxNNB4EKDHQ/view

Instruction to open source WebProject
*Notice: Before configure file. You must open WebProject.sln -> find Web.config 
-> click right mouse find <connectionStrings><add name="Product_ManagermentEntities" connectionString="metadata=res://*/dbEntities.ProductEntities.csdl|res://*/dbEntities.ProductEntities.ssdl|res://*/dbEntities.ProductEntities.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=DESKTOP-7FGEK1U;initial catalog=Product_Managerment;user id=admin123;password=admin;MultipleActiveResultSets=True;App=EntityFramework&quot;" providerName="System.Data.EntityClient" /></connectionStrings>
-> and delete it
Step 1: Find the file name ProductEntites.edmx in folder name dbEntities and detele ProductEntites.edmx
Step 2: In folder dbEntities -> press Add to create a new file -> search the ADO.NET Enity Data Model and set name is ProductEntities 
-> Next -> press New Connection -> add your sever name -> choose Authentication: SQL Sever Authentication 
-> Enter your username and password -> in connect to a database click select or enter a database name: Product_Managerment -> OK
-> After click OK the hud will back to Entity Data Model Wizard 
-> Click Yes, include the sensitive data in the connection string -> Remember to check Connection string carefully 
-> Next 
-> Click choose Tables and Stored Procedures and Functions -> Set Model Namespace is ProductEntites -> Finish
Step 3: Ctrl + S in file name ProductEntities.edmx
Step 4: Rebuild - Start 
Step 5: Waiting for load the website on localhost:44308

Link demo: https://www.youtube.com/watch?v=5tSw35fLjAs

Account to login web:
User:admin@gmail.com
Password:999999999