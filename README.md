# finHelp
Objective: Learn in-depth about C# .NET development
Project is a template React frontend 

dotnet watch run => starts the backend server

API Fundamentals:
1. Operations: Post, Get, Update, Delete

Setup:
Added VS Code extensions: C# Dev Kit, .NET Extension Pack, .NET Install Tool, NuGet Galley, Prettier, C# Extensions by JosKreativ

Define Classes: Stocks and Comments with their own attributes in the models folder

Entity Framework: Object-Relational Mapper (ORM) for .NET development
Installed Microsoft.Entity.FrameworkCore.Design, SqlServer, and Tools via NuGet Gallery Toggle

Connected Application Settings to SQL Server Management Studio and initialized the database tables

Controllers: Helps get the API endpoint for specific purpose
List vs Detail: General List for homepage but when you want more info then you go to detail page

Created API endpoints to get all stocks or get stock by id via Stock Controller

DTO: Data Tranfer Object, cleans up data when you return important data

Created API endpoint to create a new stock from body 