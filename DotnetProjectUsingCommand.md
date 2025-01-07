> List of commands to create an api and develop the same in VS code
```
dotnet new sln --name Policies

dotnet new webapi --use-controllers --name "Policies.API" --output ".\source\Policies.API"
dotnet new classlib --name "Policies.Business" --output ".\source\Policies.Business"
dotnet new classlib --name "Policies.Model" --output ".\source\Policies.Model"
dotnet new classlib --name "Policies.Repository" --output ".\source\Policies.Repository"

dotnet sln add ".\source\Policies.Business\Policies.Business.csproj"
dotnet sln add ".\source\Policies.API\Policies.API.csproj"
dotnet sln add ".\source\Policies.Model\Policies.Model.csproj"
dotnet sln add ".\source\Policies.Repository\Policies.Repository.csproj"

dotnet add ".\source\Policies.Business\Policies.Business.csproj" reference ".\source\Policies.Model\Policies.Model.csproj"
dotnet add ".\source\Policies.Business\Policies.Business.csproj" reference ".\source\Policies.Repository\Policies.Repository.csproj"
dotnet add ".\source\Policies.API\Policies.API.csproj" reference ".\source\Policies.Model\Policies.Model.csproj"
dotnet add ".\source\Policies.API\Policies.API.csproj" reference ".\source\Policies.Business\Policies.Business.csproj
dotnet add ".\source\Policies.Repository\Policies.Repository.csproj" reference ".\source\Policies.Model\Policies.Model.csproj"


dotnet build
dotnet run --project ".\source\Policies.API\Policies.API.csproj" 


dotnet --into
dotnet new list
dotnet dotnet new sln --name Policies --dry-run

```
