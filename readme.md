# The Sports Store / Pro Asp.Net Core 6
## Creating the Projects
```
dotnet new globaljson --output SportsSln/SportsStore
dotnet new web --no-https --output SportsSln/SportsStore 
dotnet new sln -o SportsSln
dotnet sln SportsSln add SportsSln/SportsStore
```
## Creating the Unit Test Project
```
dotnet new xunit -o SportsSln/SportsStore.Tests
dotnet sln SportsSln add SportsSln/SportsStore.Tests
dotnet add SportsSln/SportsStore.Tests reference SportsSln/SportsStore

dotnet add SportsSln/SportsStore.Tests package Moq
```
## Add files
```
.gitignore
readme.md
```

## Creating the Application Project Folders
- Models
- Controllers
- Views
- Views/Home
- Views/Shared

## Adding Model, Views and Controllers
see book - Chapter 7 - [Pro Asp.Net Core 6](https://learning.oreilly.com/library/view/pro-asp-net-core/9781484279571/html/338050_9_En_7_Chapter.xhtml)

## Add Entity Framework
- make sure that SQL localdb is installed (windows)
from SportsStore folder - open developer powershell
```
dotnet add package Microsoft.EntityFrameworkCore.Design 
dotnet add package Microsoft.EntityFrameworkCore.SqlServer 
dotnet tool uninstall --global dotnet-ef
dotnet tool install --global dotnet-ef 
```
A helpful site for formulating connection strings is www.connectionstrings.com.

## Create the Database Context Class 
see book - Chapter 7-16 - [Pro Asp.Net Core 6](https://learning.oreilly.com/library/view/pro-asp-net-core/9781484279571/html/338050_9_En_7_Chapter.xhtml#PC16)

## Add Repository - Interface
### new concept - IQueriable<T> vs IEnumerable<T>
see book - [Pro Asp.NET Core 6 Chapter 7.18](https://learning.oreilly.com/library/view/pro-asp-net-core/9781484279571/html/338050_9_En_7_Chapter.xhtml#:-:text=Creating%20a%20Repository) 