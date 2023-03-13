# Creating the Projects
dotnet new globaljson --output SportsSln/SportsStore
dotnet new web --no-https --output SportsSln/SportsStore 
dotnet new sln -o SportsSln
dotnet sln SportsSln add SportsSln/SportsStore

# Creating the Unit Test Project
dotnet new xunit -o SportsSln/SportsStore.Tests
dotnet sln SportsSln add SportsSln/SportsStore.Tests
dotnet add SportsSln/SportsStore.Tests reference SportsSln/SportsStore

dotnet add SportsSln/SportsStore.Tests package Moq

# Add files
.gitignore
readme.md