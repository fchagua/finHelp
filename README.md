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

Created API endpoint to create a new stock from body (POST API endpoint)
Created API endpoint to update a current stock from body based on stock id (UPDATE API endpoint)
Created API endpoint to delete a current stock from database (DELETE API endpoint)

Always try to create a new dto for the task at hand (POST, PUT) because it will help structure requests and modify code in the future

Async code can allow the program to do multiple tasks at the same time
Make sure to change any process within the async method to await if it iteracts with the database

Separate database calls from the controller with dpeendency injections with abstractions via repository
Started with getAll stocks method, can apply same technique to other methods in StockController

Refactor database related code to repository to ensure abstraction and separation of levels

Implement similar methods from stock controller and repository to comment

Data Validation:
1. Route constraints, force input from route to be a specific data type otherwise it fails
2. Data Validation Annotations in Dtos

Data Filtering
Can add QueryObject class to help filter what data based on parameters and then use it in getAll method

Data Sorting
Can add SortBy and isDescending parameters to QueryObject class to allow sorting and then implment in repository

Pagination
1. Dont return all results at once 
2. break data into pages
.Skip(2) = skip first 2 elements and take remaining elements
.Take(2) = take first 2 elements
.Skip(2).Take(2) = develops pagination 

JWT for Users
Each user will log in with email and password
Application will issue the user a jwt string which it will need to validate
JWT contains header, payload, and secret that is all encrypted
Packages to install: MS.Extensions.Identity.Core, MS.AspNETCore.Identity.EntityFrameworkCore, and MS.AspNetCore.Authentication.JwtBearer

Identity will provide IdentityUser class with Password, Email, Bio. You can extend the class later on if needed.

UserManager will help manage username and passwords for account login

Create service to generate tokens

Claims: authentication wallet, more generic and broad (old school)

Roles: tag associated with the user, dont require DB and very flexible (new school)

MS has moved away from Roles

Generate JWT on the server and fill it with claims that act like roles which describes the user and what he can do

Process:
User logs in with email and password
Send JWT to server
Once authenticated, ClaimsPrincipal is created

Login Task:
User and Signing manager to find user and check password

Added Swagger config to allow visualization of Authorized account
