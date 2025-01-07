
```

>dotnet --info

note: to get information about the dotnet 

1.use this command to create a solution , check with dryrun if looks good remove dryrun and excute it

>dotnet new sln --name Policy --dry-run

2. To add the project your need to know the list of template , and you may see all the list using this commnad
>dotnet new list

3. if you want to create a web api ( webapi) teamplate can be used ,to create by this commnad

> dotnet new webapi --controllers --name "Dell.Astra.Policies.API" --output ".\source\Dell.Astra.Policies.API" --dry-run

[validat the files going to be created and if it looks good , remove --dry-run and execute it]

4. if you want to add differnet layers(business) as class library (classlib) template can be used to created by this commnad

> dotnet new classlib --name "Dell.Astra.Policies.Business" --output ".\source\Dell.Astra.Policies.Business" --dry-run

[validate the files created and location of the file if looks good then remove dryrun and execute it ]

5. if you want to add differnet layers ( Model) as class library (classlib) template can be used to created by this commnad

> dotnet new classlib --name "Dell.Astra.Policies.Model" --output ".\source\Dell.Astra.Policies.Model" --dry-run

[validate the files created and location of the file if looks good then remove dryrun and execute it ]
 
6. if you want to add differnet layers ( Repository ) as class library (classlib) template can be used to created by this commnad

> dotnet new classlib --name "Dell.Astra.Policies.Repository" --output ".\source\Dell.Astra.Policies.Repository" --dry-run

[validate the files created and location of the file if looks good then remove dryrun and execute it ]

7. Add all the projects to the solution we created 
> dotnet sln add ".\source\Dell.Astra.Policies.Business\Dell.Astra.Policies.Business.csproj" "\source\Dell.Astra.Policies.API\Dell.Astra.Policies.API.csproj" ".\source\Dell.Astra.Policies.Model\Dell.Astra.Policies.Model.csproj" ".\source\Dell.Astra.Policies.Repository\Dell.Astra.Policies.Repository.csproj"

or 
dotnet sln add ".\source\Dell.Astra.Policies.Business\Dell.Astra.Policies.Business.csproj"
dotnet sln add "\source\Dell.Astra.Policies.API\Dell.Astra.Policies.API.csproj"
dotnet sln add ".\source\Dell.Astra.Policies.Model\Dell.Astra.Policies.Model.csproj"
dotnet sln add ".\source\Dell.Astra.Policies.Repository\Dell.Astra.Policies.Repository.csproj"

8. Build the project
> dotnet build

9. Run the project
>dotnet run --project ".\source\Dell.Astra.Policies.API\Dell.Astra.Policies.API.csproj" 

if you want to run in watch mode, 
>dotnet watch --project ".\source\Dell.Astra.Policies.API\\Dell.Astra.Policies.API.csproj"

[the project your want to start by default can be given the path]

10. add project reference to use further , for the same

>dotnet add ".\source\Dell.Astra.Policies.Business\Dell.Astra.Policies.Business.csproj" reference ".\source\Dell.Astra.Policies.Model\Dell.Astra.Policies.Model.csproj"
>dotnet add ".\source\Dell.Astra.Policies.Business\Dell.Astra.Policies.Business.csproj" reference ".\source\Dell.Astra.Policies.Repository\Dell.Astra.Policies.Repository.csproj"

>dotnet add ".\source\Dell.Astra.Policies.API\Dell.Astra.Policies.API.csproj" reference ".\source\Dell.Astra.Policies.Model\Dell.Astra.Policies.Model.csproj"
>dotnet add ".\source\Dell.Astra.Policies.API\Dell.Astra.Policies.API.csproj" reference ".\source\Dell.Astra.Policies.Business\Dell.Astra.Policies.Business.csproj

11. if https is not working

>dotnet dev-certs https --trust

in admin mode , if this not works , use this
> dotnet dev-certs https --clean


```
