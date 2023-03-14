# Creating the Projects
```
dotnet new globaljson --output SportsSln/SportsStore
dotnet new web --no-https --output SportsSln/SportsStore 
dotnet new sln -o SportsSln
dotnet sln SportsSln add SportsSln/SportsStore
```
# Creating the Unit Test Project
```
dotnet new xunit -o SportsSln/SportsStore.Tests
dotnet sln SportsSln add SportsSln/SportsStore.Tests
dotnet add SportsSln/SportsStore.Tests reference SportsSln/SportsStore

dotnet add SportsSln/SportsStore.Tests package Moq
```
# Add files
```
.gitignore
readme.md
```

# Creating the Application Project Folders
Models
Controllers
Views
Views/Home
Views/Shared

# Add Entity Framework
- make sure that SQL localdb is installed (windows)
from SportsStore folder - open developer powershell
```
dotnet add package Microsoft.EntityFrameworkCore.Design 
dotnet add package Microsoft.EntityFrameworkCore.SqlServer 
dotnet tool uninstall --global dotnet-ef
dotnet tool install --global dotnet-ef 
```