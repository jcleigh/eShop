# .NET 9.0 Upgrade Report

## Project target framework modifications

| Project name                                    | Old Target Framework                                                                                              | New Target Framework                                                                                                    | Commits                   |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|---------------------------|
| EventBus.csproj                                 | net8.0                                                                                                            | net9.0                                                                                                                  | 5e9c6dd5                  |
| Ordering.Domain.csproj                          | net8.0                                                                                                            | net9.0                                                                                                                  | cfdc5b16                  |
| IntegrationEventLogEF.csproj                    | net8.0                                                                                                            | net9.0                                                                                                                  | c1105960                  |
| Ordering.Infrastructure.csproj                  | net8.0                                                                                                            | net9.0                                                                                                                  | cb34c8ac                  |
| EventBusRabbitMQ.csproj                         | net8.0                                                                                                            | net9.0                                                                                                                  | 18e0ddd1                  |
| eShop.ServiceDefaults.csproj                    | net8.0                                                                                                            | net9.0                                                                                                                  | 8b680556                  |
| WebAppComponents.csproj                         | net8.0                                                                                                            | net9.0                                                                                                                  | 2380dbc3                  |
| ClientApp.csproj                                | net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0;net8.0-windows10.0.19041.0                                  | net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0;net8.0-windows10.0.19041.0;net9.0-windows                       | 44178589                  |
| Ordering.API.csproj                             | net8.0                                                                                                            | net9.0                                                                                                                  | 55b9039c                  |
| Identity.API.csproj                             | net8.0                                                                                                            | net9.0                                                                                                                  | e1927315                  |
| Catalog.API.csproj                              | net8.0                                                                                                            | net9.0                                                                                                                  | af61e8ed                  |
| Basket.API.csproj                               | net8.0                                                                                                            | net9.0                                                                                                                  | f9c82814                  |
| OrderProcessor.csproj                           | net8.0                                                                                                            | net9.0                                                                                                                  | bcddd190                  |
| PaymentProcessor.csproj                         | net8.0                                                                                                            | net9.0                                                                                                                  | 4c996b98                  |
| WebhookClient.csproj                            | net8.0                                                                                                            | net9.0                                                                                                                  | 21526c04                  |
| Mobile.Bff.Shopping.csproj                      | net8.0                                                                                                            | net9.0                                                                                                                  | 91efb93b                  |
| WebApp.csproj                                   | net8.0                                                                                                            | net9.0                                                                                                                  | 43544d04                  |
| Webhooks.API.csproj                             | net8.0                                                                                                            | net9.0                                                                                                                  | 1d1302b2                  |
| HybridApp.csproj                                | net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0-windows10.0.19041.0                                         | net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0-windows10.0.19041.0;net9.0-windows                               | a54434df                  |
| Ordering.UnitTests.csproj                       | net8.0                                                                                                            | net9.0                                                                                                                  | cb621ea2                  |
| Ordering.FunctionalTests.csproj                 | net8.0                                                                                                            | net9.0                                                                                                                  | d32e550d                  |
| Catalog.FunctionalTests.csproj                  | net8.0                                                                                                            | net9.0                                                                                                                  | 04de2258                  |
| Basket.UnitTests.csproj                         | net8.0                                                                                                            | net9.0                                                                                                                  | f231f943                  |
| eShop.AppHost.csproj                            | net8.0                                                                                                            | net9.0                                                                                                                  | 06c2f1ec                  |

## NuGet Packages

| Package Name                                        | Old Version                 | New Version                     | Commit ID                                 |
|:----------------------------------------------------|:---------------------------:|:-------------------------------:|-------------------------------------------|
| Aspire.Azure.AI.OpenAI                             | 8.0.0-preview.8.24258.2     | 9.4.0-preview.1.25378.8         | ee4ec7bf                                  |
| Aspire.Hosting.AppHost                              | 8.2.0                       | 9.4.0                           | dd79a78c, c886633d                       |
| Aspire.Hosting.Azure.CognitiveServices             | 8.2.0                       | 9.4.0                           | c886633d                                  |
| Aspire.Hosting.PostgreSQL                          | 8.2.0                       | 9.4.0                           | dd79a78c, c886633d                       |
| Aspire.Hosting.RabbitMQ                            | 8.2.0                       | 9.4.0                           | c886633d                                  |
| Aspire.Hosting.Redis                               | 8.2.0                       | 9.4.0                           | c886633d                                  |
| Aspire.Npgsql                                      | 8.2.0                       | 9.4.0                           | 89d0a82b                                  |
| Aspire.Npgsql.EntityFrameworkCore.PostgreSQL       | 8.2.0                       | 9.4.0                           | f0f69c79, d194fb5f, ee4ec7bf, 4acc440a   |
| Aspire.RabbitMQ.Client                             | 8.2.0                       | 9.4.0                           | 653015c3                                  |
| Aspire.StackExchange.Redis                         | 8.2.0                       | 9.4.0                           | 69b92976                                  |
| Duende.IdentityServer                              | 7.0.6                       | 7.2.4                           | d194fb5f                                  |
| FluentValidation.AspNetCore                        | 11.3.0                      | 11.3.1                          | f0f69c79                                  |
| Microsoft.AspNetCore.Authentication.JwtBearer      | 8.0.7                       | 9.0.8                           | 964b0c9b                                  |
| Microsoft.AspNetCore.Authentication.OpenIdConnect  | 8.0.7                       | 9.0.8                           | 20c74ac4                                  |
| Microsoft.AspNetCore.Components.QuickGrid          | 8.0.7                       | 9.0.8                           | 20c74ac4                                  |
| Microsoft.AspNetCore.Components.Web                | 8.0.7                       | 9.0.8                           | b182e061                                  |
| Microsoft.AspNetCore.Identity.EntityFrameworkCore  | 8.0.7                       | 9.0.8                           | d194fb5f                                  |
| Microsoft.AspNetCore.Identity.UI                   | 8.0.7                       | 9.0.8                           | d194fb5f                                  |
| Microsoft.AspNetCore.Mvc.Testing                   | 8.0.7                       | 9.0.8                           | dd79a78c                                  |
| Microsoft.AspNetCore.OpenApi                       | 8.0.7                       | 9.0.8                           | 964b0c9b                                  |
| Microsoft.AspNetCore.TestHost                      | 8.0.7                       | 9.0.8                           | dd79a78c                                  |
| Microsoft.EntityFrameworkCore.Tools                | 8.0.8                       | 9.0.8                           | f0f69c79, d194fb5f, ee4ec7bf, 4acc440a   |
| Microsoft.Extensions.DependencyInjection.Abstractions | 8.0.1                    | 9.0.8                           | 075b212c                                  |
| Microsoft.Extensions.Http                          | 8.0.0                       | 9.0.8                           | 89697900                                  |
| Microsoft.Extensions.Http.Resilience               | 8.7.0                       | 9.7.0                           | 964b0c9b                                  |
| Microsoft.Extensions.Identity.Stores               | 8.0.7                       | 9.0.8                           | 7bd415ed                                  |
| Microsoft.Extensions.Logging.Debug                 | 8.0.*-*                     | 9.0.8                           | b39e24d0                                  |
| Microsoft.Extensions.Options                       | 8.0.2                       | 9.0.8                           | 075b212c                                  |
| Microsoft.Extensions.Options.ConfigurationExtensions | 8.0.0                     | 9.0.8                           | 653015c3                                  |
| Microsoft.Extensions.ServiceDiscovery              | 8.2.0                       | 9.4.0                           | 964b0c9b                                  |
| Microsoft.Extensions.ServiceDiscovery.Yarp         | 8.2.0                       | 9.4.0                           | d25717e3                                  |
| Npgsql.EntityFrameworkCore.PostgreSQL              | 8.0.4                       | 9.0.4                           | 962b89d8                                  |
| OpenTelemetry.Instrumentation.AspNetCore           | 1.9.0                       | 1.12.0                          | 964b0c9b                                  |
| OpenTelemetry.Instrumentation.Http                 | 1.9.0                       | 1.12.0                          | 964b0c9b                                  |
| Polly.Core                                         | 8.4.1                       | 8.6.2                           | 82d59097                                  |
| System.Reflection.TypeExtensions                   | 4.7.0                       | Removed                         | 12fb0ec0                                  |

## All commits

| Commit ID              | Description                                |
|:-----------------------|:-------------------------------------------|
| 345c00c4               | Commit upgrade plan                        |
| 559826d6               | Store final changes for step              |
| 5e9c6dd5               | Update EventBus.csproj to target net9.0   |
| 075b212c               | Update package versions in Directory.Packages.props |
| cfdc5b16               | Update Ordering.Domain.csproj to target net9.0 |
| 12fb0ec0               | Remove unused package from Ordering.Domain.csproj |
| c1105960               | Update target framework to net9.0 in IntegrationEventLogEF.csproj |
| cb34c8ac               | Update target framework to net9.0 in Ordering.Infrastructure.csproj |
| 18e0ddd1               | Update EventBusRabbitMQ.csproj to target net9.0 |
| 653015c3               | Update package versions in Directory.Packages.props |
| 8b680556               | Update target framework to net9.0 in eShop.ServiceDefaults.csproj |
| 964b0c9b               | Update package versions and add Polly.Core dependency |
| 2380dbc3               | Update target framework to net9.0 in WebAppComponents.csproj |
| b182e061               | Set fixed version for Components.Web in Directory.Packages.props |
| 44178589               | Clean up formatting in ClientApp.csproj file |
| b39e24d0               | Update logging package version in ClientApp.csproj |
| 1ba1e3fc               | Remove BOM from XAML files for consistency |
| 55b9039c               | Update Ordering.API.csproj to target net9.0 |
| f0f69c79               | Update package versions and add overrides in Ordering.API |
| e1927315               | Update Identity.API.csproj to target .NET 9.0 |
| d194fb5f               | Update package versions and add new dependencies |
| af61e8ed               | Upgrade target framework to net9.0 in Catalog.API.csproj |
| ee4ec7bf               | Update package versions and add dependencies |
| f9c82814               | Update target framework to net9.0 in Basket.API.csproj |
| 69b92976               | Update Redis package version and add Polly.Core |
| bcddd190               | Update target framework to net9.0 in OrderProcessor.csproj |
| 89d0a82b               | Update Npgsql version and add Polly.Core to OrderProcessor |
| 4c996b98               | Update PaymentProcessor.csproj to target .NET 9.0 |
| 82d59097               | Update Polly.Core version in Directory.Packages.props |
| 20c74ac4               | Update package versions in Directory.Packages.props |
| 21526c04               | Update WebhookClient.csproj to target .NET 9.0 |
| 91efb93b               | Update target framework to net9.0 in Mobile.Bff.Shopping.csproj |
| d25717e3               | Set fixed Yarp ServiceDiscovery version in Directory.Packages.props |
| 43544d04               | Update target framework to net9.0 in WebApp.csproj |
| d13790ea               | Add Yarp.ReverseProxy to WebApp.csproj dependencies |
| 1d1302b2               | Update target framework to net9.0 in Webhooks.API.csproj |
| 4acc440a               | Add Npgsql.EntityFrameworkCore.PostgreSQL to Webhooks.API.csproj |
| a54434df               | Refactor HybridApp.csproj: reformat and clean up XML |
| 89697900               | Remove WebAppComponents project reference from HybridApp.csproj |
| ca444e46               | Remove BOM from XAML files for consistency |
| cb621ea2               | Update target framework to net9.0 in Ordering.UnitTests.csproj |
| 962b89d8               | Update Npgsql.EntityFrameworkCore.PostgreSQL in Directory.Packages.props |
| d32e550d               | Update target framework to net9.0 in Ordering.FunctionalTests.csproj |
| dd79a78c               | Update package versions and add new test dependencies |
| 3c1e6cf3               | Update GrpcVersion in Directory.Packages.props to 2.71.0 |
| 04de2258               | Update target framework to net9.0 in Catalog.FunctionalTests.csproj |
| 76a94595               | Add new package references in Catalog.FunctionalTests.csproj |
| f231f943               | Update Basket.UnitTests.csproj to target net9.0 |
| 7bd415ed               | Update Microsoft.Extensions.Identity.Stores version in Directory.Packages.props |
| 06c2f1ec               | Update target framework to net9.0 in eShop.AppHost.csproj |
| c886633d               | Update package versions and add new dependencies |

## Project feature upgrades

### System.Reflection.TypeExtensions Package Removal

The System.Reflection.TypeExtensions package was successfully removed from the Ordering.Domain project as its functionality is now included with the .NET 9.0 framework reference.

### Security Vulnerability Resolved

Successfully upgraded Duende.IdentityServer from version 7.0.6 to 7.2.4 in the Identity.API project, resolving the identified security vulnerability.

### Aspire Package Modernization

All deprecated Aspire 8.x packages were successfully upgraded to the latest 9.4.0 versions, including:
- Aspire.Hosting.* packages (AppHost, PostgreSQL, RabbitMQ, Redis, Azure.CognitiveServices)
- Aspire.Npgsql and Aspire.Npgsql.EntityFrameworkCore.PostgreSQL
- Aspire.RabbitMQ.Client and Aspire.StackExchange.Redis

### Multi-Targeting Platform Projects

ClientApp and HybridApp projects were successfully updated to include .NET 9.0 Windows target while maintaining compatibility with existing mobile platforms:
- ClientApp: Added net9.0-windows to existing mobile targets
- HybridApp: Added net9.0-windows to existing mobile targets and removed incompatible WebAppComponents reference

### File Encoding Standardization

Byte Order Mark (BOM) was removed from XAML files in both ClientApp and HybridApp projects to improve cross-platform compatibility and consistency.

## Next steps

- **Test the application**: Run comprehensive tests to ensure all functionality works correctly with .NET 9.0
- **Performance validation**: Verify that the application performs as expected with the new runtime
- **Monitor for any runtime issues**: Keep an eye on logs and application behavior in the new environment
- **Consider .NET 9.0 specific features**: Explore new .NET 9.0 features that could benefit the application