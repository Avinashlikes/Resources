To add EF in dotnet core -

> Add  dependency
```
	dotnet add pacakage Microsoft.EntityFrameworkCore
	dotnet add pacakage Microsoft.EntityFrameworkCore.SqlServer
	dotnet add pacakage Microsoft.EntityFrameworkCore.Tools
```
> Create a Class

> Add Db context class in Model or Entity and inherit from DbContext e.g:

	``` public class CustomerContext : DbContext
    {
        public CustomerContext(DbContextOptions options) : base(options)
        {
        }
        public DbSet<Customer> Customers {get;set;} = null;

    } ```
	
> Configure data base connection

 ``` "ConnectionStrings": {
    "NorthwindContext":"data source=localhost;initial catalog=Northwind;persist security info=True;Integrated Security=SSPI;TrustServerCertificate=True"
  } ```
	
> Add DB context in builder 

``` // add db context

builder.Services.AddDbContext<CustomerContext>(Option=>
        Option.UseSqlServer(builder.Configuration.GetConnectionString("NorthwindContext")));

```
> Reolve the Interfaces if any in middleware.
```
builder.Services.AddScoped<ICustomerRepository, CustomerRepository>();
builder.Services.AddScoped<ICustomerService, CustomerService>();
```
