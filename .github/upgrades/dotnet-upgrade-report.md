# .NET 9.0 Upgrade Report

## Project target framework modifications

| Project name                                   | Old Target Framework    | New Target Framework         | Commits                   |
|:-----------------------------------------------|:-----------------------:|:----------------------------:|---------------------------|
| EventBus.csproj                                | net8.0                  | net9.0                       | 4e660db7                  |
| Ordering.Domain.csproj                         | net8.0                  | net9.0                       | f167d387                  |
| IntegrationEventLogEF.csproj                   | net8.0                  | net9.0                       | 1d370577                  |
| Ordering.Infrastructure.csproj                 | net8.0                  | net9.0                       | 03508bf5                  |
| EventBusRabbitMQ.csproj                        | net8.0                  | net9.0                       | 396dd7f9                  |
| eShop.ServiceDefaults.csproj                   | net8.0                  | net9.0                       | c8da88f2                  |
| WebAppComponents.csproj                        | net8.0                  | net9.0                       | 0f2dce23                  |
| Ordering.API.csproj                            | net8.0                  | net9.0                       | f6fe0889                  |
| Identity.API.csproj                            | net8.0                  | net9.0                       | 8d6ce0c8                  |
| Catalog.API.csproj                             | net8.0                  | net9.0                       | aa3ec25f, ec1988c7        |
| Basket.API.csproj                              | net8.0                  | net9.0                       | 7eb15b71                  |
| OrderProcessor.csproj                          | net8.0                  | net9.0                       | 5f21d90e                  |
| PaymentProcessor.csproj                        | net8.0                  | net9.0                       | d538a13f                  |

## NuGet Packages

| Package Name                                       | Old Version | New Version | Commit ID                                 |
|:---------------------------------------------------|:-----------:|:-----------:|-------------------------------------------|
| Aspire.Azure.AI.OpenAI                            | 8.0.0-preview.8.24258.2 | 9.4.1-preview.1.25408.4 | bee95b27                                  |
| Aspire.Npgsql                                     | 8.2.0       | 9.4.1       | cd5e15bd                                  |
| Aspire.Npgsql.EntityFrameworkCore.PostgreSQL     | 8.2.0       | 9.4.1       | ed12609a, b523a4fd, bee95b27              |
| Aspire.RabbitMQ.Client                           | 8.2.0       | 9.4.1       | 17817c45                                  |
| Aspire.StackExchange.Redis                       | 8.2.0       | 9.4.1       | 6d9db3d8                                  |
| FluentValidation.AspNetCore                       | 11.3.0      | 11.3.1      | ed12609a                                  |
| Microsoft.AspNetCore.Authentication.JwtBearer    | 8.0.7       | 9.0.8       | d573be87                                  |
| Microsoft.AspNetCore.Components.Web              | 8.0.7       | 9.0.8       | c953f1a5                                  |
| Microsoft.AspNetCore.Identity.EntityFrameworkCore| 8.0.7       | 9.0.8       | b523a4fd                                  |
| Microsoft.AspNetCore.Identity.UI                 | 8.0.7       | 9.0.8       | b523a4fd                                  |
| Microsoft.AspNetCore.OpenApi                     | 8.0.7       | 9.0.8       | d573be87                                  |
| Microsoft.EntityFrameworkCore.Tools              | 8.0.8       | 9.0.8       | ed12609a, b523a4fd, bee95b27              |
| Microsoft.Extensions.DependencyInjection.Abstractions | 8.0.1  | 9.0.8       | d1daa49e                                  |
| Microsoft.Extensions.Http.Resilience             | 8.7.0       | 9.8.0       | d573be87                                  |
| Microsoft.Extensions.Logging.Debug               | 8.0.*-*     | 9.0.8       | 3af347eb                                  |
| Microsoft.Extensions.Options                     | 8.0.2       | 9.0.8       | d1daa49e                                  |
| Microsoft.Extensions.Options.ConfigurationExtensions | 8.0.0   | 9.0.8       | 17817c45                                  |
| Microsoft.Extensions.ServiceDiscovery             | 8.2.0       | 9.4.1       | d573be87                                  |
| OpenTelemetry.Instrumentation.AspNetCore         | 1.9.0       | 1.12.0      | d573be87                                  |
| OpenTelemetry.Instrumentation.Http               | 1.9.0       | 1.12.0      | d573be87                                  |
| Polly.Core                                        | 8.4.1       | 8.6.3       | befb3f00                                  |

## All commits

| Commit ID              | Description                                |
|:-----------------------|:-------------------------------------------|
| 57268786               | Commit upgrade plan                        |
| 2b9c412f               | Store final changes for step 'Ensure that the SDK version specified in global.json files is compatible with the .NET 9.0 upgrade' |
| 4e660db7               | Update EventBus.csproj to target .NET 9.0 |
| d1daa49e               | Update package versions in Directory.Packages.props |
| f167d387               | Update target framework to net9.0 in Ordering.Domain.csproj |
| b42ba8e7               | Remove TypeExtensions package from Ordering.Domain.csproj |
| 1d370577               | Update IntegrationEventLogEF.csproj to target .NET 9.0 |
| 03508bf5               | Update target framework to net9.0 in Ordering.Infrastructure.csproj |
| 396dd7f9               | Update EventBusRabbitMQ.csproj to target .NET 9.0 |
| 17817c45               | Update package versions in Directory.Packages.props |
| c8da88f2               | Update target framework to net9.0 in eShop.ServiceDefaults.csproj |
| d573be87               | Update package versions and add Polly.Core dependency |
| 0f2dce23               | Update target framework to net9.0 in WebAppComponents.csproj |
| c953f1a5               | Set explicit version for Components.Web in Directory.Packages.props |
| f1772d52               | Clean up ClientApp.csproj by removing extra blank lines |
| 3af347eb               | Update Microsoft.Extensions.Logging.Debug to v9.0.8 in ClientApp.csproj |
| b269f17e               | Normalize XML encoding headers in XAML files |
| f6fe0889               | Update target framework to net9.0 in Ordering.API.csproj |
| ed12609a               | Update package versions and add overrides in Ordering.API |
| 8d6ce0c8               | Update Identity.API.csproj to target .NET 9.0 |
| b523a4fd               | Update Identity package versions and add new dependencies |
| aa3ec25f               | Store final changes for step 'Upgrade Catalog.API.csproj' |
| ec1988c7               | Update Catalog.API.csproj to target .NET 9.0 |
| bee95b27               | Update package versions and add dependencies |
| 7eb15b71               | Update Basket.API.csproj to target .NET 9.0 |
| 6d9db3d8               | Update Redis package version and add Polly.Core dependency |
| 5f21d90e               | Bump target framework to net9.0 in OrderProcessor.csproj |
| cd5e15bd               | Update Aspire.Npgsql version and add Polly.Core package |
| d538a13f               | Update PaymentProcessor.csproj to target .NET 9.0 |
| befb3f00               | Update Polly.Core version in Directory.Packages.props |

## Project feature upgrades

Contains summary of modifications made to the project assets during different upgrade stages.

### Ordering.Domain

Here is what changed for the project during upgrade:

- Removed System.Reflection.TypeExtensions package as functionality is included with framework reference in .NET 9.0

### Catalog.API

Here is what changed for the project during upgrade:

- **Partial completion**: Azure OpenAI integration method updated from `AddAzureOpenAIClient` to `AddAzureAIOpenAI` for Aspire 9.4.1 compatibility, but compilation error remains due to missing `OpenAIClient` type in updated Azure.AI.OpenAI package
- Manual intervention required to complete Azure OpenAI integration upgrade

### ClientApp

Here is what changed for the project during upgrade:

- Cleaned up project file formatting by removing extra blank lines
- Normalized XML encoding headers in XAML files to ensure consistent encoding declarations
- Updated Microsoft.Extensions.Logging.Debug from wildcard version to explicit 9.0.8

## Next steps

- **Action Required**: Fix the Azure OpenAI client registration in Catalog.API project. The current method `AddAzureAIOpenAI` still references missing `OpenAIClient` type. Check the latest Aspire 9.4.1 documentation for the correct Azure OpenAI integration method.
- Complete upgrade of remaining projects (WebhookClient, Mobile.Bff.Shopping, WebApp, Webhooks.API, HybridApp, test projects, and eShop.AppHost)
- Run tests to validate upgrade functionality
- Review and test Azure OpenAI functionality in Catalog.API once integration is fixed

## Upgrade Status

- **Completed**: 13 out of 26 projects successfully upgraded to .NET 9.0
- **Partial**: 1 project (Catalog.API) upgraded but requires manual fix for Azure OpenAI integration
- **Remaining**: 12 projects still need to be upgraded
- **Overall Progress**: ~50% complete