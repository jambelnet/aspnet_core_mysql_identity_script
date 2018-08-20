# ASP.NET Core Identity script for MySql

[Gist](https://gist.github.com/jambelnet/1ea70236c933d644b36895b296fb44e5)

### Table structure for:
* AspNetRoles
* AspNetUserClaims
* AspNetUserLogins
* AspNetUserRoles
* AspNetUsers
* AspNetUserTokens

### On Startup.cs
 `public void ConfigureServices(IServiceCollection services)
  {
      services.AddDbContext<ApplicationDbContext>(options =>
          options.UseMySQL(Configuration.GetConnectionString("DefaultConnection")));
      ...
  }`
        
### On appsettings.json
 `"ConnectionStrings": {
		"DefaultConnection": "server=<your_server>;userid=root;password=<your_db_pass>;database=<your_db_name>;"
	},`


Install ***MySql.Data.EntityFrameworkCore*** package for Entity Framework
