# .NET 9.0 Upgrade Plan

## Execution Steps

Execute steps below sequentially one by one in the order they are listed.

1. Validate that an .NET 9.0 SDK required for this upgrade is installed on the machine and if not, help to get it installed.
2. Ensure that the SDK version specified in global.json files is compatible with the .NET 9.0 upgrade.
3. Upgrade src\EventBus\EventBus.csproj
4. Upgrade src\Ordering.Domain\Ordering.Domain.csproj
5. Upgrade src\IntegrationEventLogEF\IntegrationEventLogEF.csproj
6. Upgrade src\Ordering.Infrastructure\Ordering.Infrastructure.csproj
7. Upgrade src\EventBusRabbitMQ\EventBusRabbitMQ.csproj
8. Upgrade src\eShop.ServiceDefaults\eShop.ServiceDefaults.csproj
9. Upgrade src\WebAppComponents\WebAppComponents.csproj
10. Upgrade src\ClientApp\ClientApp.csproj
11. Upgrade src\Ordering.API\Ordering.API.csproj
12. Upgrade src\Identity.API\Identity.API.csproj
13. Upgrade src\Catalog.API\Catalog.API.csproj
14. Upgrade src\Basket.API\Basket.API.csproj
15. Upgrade src\OrderProcessor\OrderProcessor.csproj
16. Upgrade src\PaymentProcessor\PaymentProcessor.csproj
17. Upgrade src\WebhookClient\WebhookClient.csproj
18. Upgrade src\Mobile.Bff.Shopping\Mobile.Bff.Shopping.csproj
19. Upgrade src\WebApp\WebApp.csproj
20. Upgrade src\Webhooks.API\Webhooks.API.csproj
21. Upgrade src\HybridApp\HybridApp.csproj
22. Upgrade tests\Ordering.UnitTests\Ordering.UnitTests.csproj
23. Upgrade tests\Ordering.FunctionalTests\Ordering.FunctionalTests.csproj
24. Upgrade tests\Catalog.FunctionalTests\Catalog.FunctionalTests.csproj
25. Upgrade tests\Basket.UnitTests\Basket.UnitTests.csproj
26. Upgrade src\eShop.AppHost\eShop.AppHost.csproj

## Settings

This section contains settings and data used by execution steps.

### Aggregate NuGet packages modifications across all projects

NuGet packages used across all selected projects or their dependencies that need version update in projects that reference them.

| Package Name                                        | Current Version           | New Version                      | Description                                         |
|:----------------------------------------------------|:-------------------------:|:--------------------------------:|:----------------------------------------------------|
| Aspire.Azure.AI.OpenAI                             | 8.0.0-preview.8.24258.2   | 9.4.0-preview.1.25378.8          | Recommended for .NET 9.0                           |
| Aspire.Hosting.AppHost                              | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.Hosting.Azure.CognitiveServices             | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.Hosting.PostgreSQL                          | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.Hosting.RabbitMQ                            | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.Hosting.Redis                               | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.Npgsql                                      | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.Npgsql.EntityFrameworkCore.PostgreSQL       | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.RabbitMQ.Client                             | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Aspire.StackExchange.Redis                         | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Duende.IdentityServer                              | 7.0.6                     | 7.2.4                            | Security vulnerability                              |
| FluentValidation.AspNetCore                        | 11.3.0                    | 11.3.1                           | Deprecated package                                  |
| Microsoft.AspNetCore.Authentication.JwtBearer      | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.Authentication.OpenIdConnect  | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.Components.QuickGrid          | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.Components.Web                | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.Identity.EntityFrameworkCore  | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.Identity.UI                   | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.Mvc.Testing                   | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.OpenApi                       | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.AspNetCore.TestHost                      | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.EntityFrameworkCore.Tools                | 8.0.8                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.DependencyInjection.Abstractions | 8.0.1                  | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.Http                          | 8.0.0                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.Http.Resilience               | 8.7.0                     | 9.7.0                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.Identity.Stores               | 8.0.7                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.Logging.Debug                 | 8.0.*-*; 8.0.0            | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.Options                       | 8.0.2                     | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.Options.ConfigurationExtensions | 8.0.0                   | 9.0.8                            | Recommended for .NET 9.0                           |
| Microsoft.Extensions.ServiceDiscovery              | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| Microsoft.Extensions.ServiceDiscovery.Yarp         | 8.2.0                     | 9.4.0                            | Deprecated package - out of support                |
| OpenTelemetry.Instrumentation.AspNetCore           | 1.9.0                     | 1.12.0                           | Recommended for .NET 9.0                           |
| OpenTelemetry.Instrumentation.Http                 | 1.9.0                     | 1.12.0                           | Recommended for .NET 9.0                           |

### Project upgrade details

This section contains details about each project upgrade and modifications that need to be done in the project.

#### EventBus modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Microsoft.Extensions.DependencyInjection.Abstractions should be updated from `8.0.1` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.Extensions.Options should be updated from `8.0.2` to `9.0.8` (*recommended for .NET 9.0*)

#### Ordering.Domain modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

Other changes:
  - System.Reflection.TypeExtensions package functionality is included with framework reference

#### IntegrationEventLogEF modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

#### Ordering.Infrastructure modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

#### EventBusRabbitMQ modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.RabbitMQ.Client should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Microsoft.Extensions.Options.ConfigurationExtensions should be updated from `8.0.0` to `9.0.8` (*recommended for .NET 9.0*)

#### eShop.ServiceDefaults modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Microsoft.AspNetCore.OpenApi should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.AspNetCore.Authentication.JwtBearer should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.Extensions.Http.Resilience should be updated from `8.7.0` to `9.7.0` (*recommended for .NET 9.0*)
  - Microsoft.Extensions.ServiceDiscovery should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - OpenTelemetry.Instrumentation.AspNetCore should be updated from `1.9.0` to `1.12.0` (*recommended for .NET 9.0*)
  - OpenTelemetry.Instrumentation.Http should be updated from `1.9.0` to `1.12.0` (*recommended for .NET 9.0*)

#### WebAppComponents modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Microsoft.AspNetCore.Components.Web should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)

#### ClientApp modifications

Project properties changes:
  - Target frameworks should be changed from `net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0;net8.0-windows10.0.19041.0` to `net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0;net8.0-windows10.0.19041.0;net9.0-windows`

NuGet packages changes:
  - Microsoft.Extensions.Logging.Debug should be updated from `8.0.*-*` to `9.0.8` (*recommended for .NET 9.0*)

#### Ordering.API modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Npgsql.EntityFrameworkCore.PostgreSQL should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Microsoft.EntityFrameworkCore.Tools should be updated from `8.0.8` to `9.0.8` (*recommended for .NET 9.0*)
  - FluentValidation.AspNetCore should be updated from `11.3.0` to `11.3.1` (*deprecated package*)

#### Identity.API modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Microsoft.AspNetCore.Identity.EntityFrameworkCore should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.AspNetCore.Identity.UI should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.EntityFrameworkCore.Tools should be updated from `8.0.8` to `9.0.8` (*recommended for .NET 9.0*)
  - Aspire.Npgsql.EntityFrameworkCore.PostgreSQL should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Duende.IdentityServer should be updated from `7.0.6` to `7.2.4` (*security vulnerability*)

#### Catalog.API modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Npgsql.EntityFrameworkCore.PostgreSQL should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Microsoft.EntityFrameworkCore.Tools should be updated from `8.0.8` to `9.0.8` (*recommended for .NET 9.0*)
  - Aspire.Azure.AI.OpenAI should be updated from `8.0.0-preview.8.24258.2` to `9.4.0-preview.1.25378.8` (*recommended for .NET 9.0*)

#### Basket.API modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.StackExchange.Redis should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)

#### OrderProcessor modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Npgsql should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)

#### PaymentProcessor modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

#### WebhookClient modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Microsoft.AspNetCore.Authentication.OpenIdConnect should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.AspNetCore.Components.QuickGrid should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)

#### Mobile.Bff.Shopping modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Microsoft.Extensions.ServiceDiscovery.Yarp should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)

#### WebApp modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Azure.AI.OpenAI should be updated from `8.0.0-preview.8.24258.2` to `9.4.0-preview.1.25378.8` (*recommended for .NET 9.0*)
  - Microsoft.Extensions.ServiceDiscovery.Yarp should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Microsoft.AspNetCore.Authentication.OpenIdConnect should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)

#### Webhooks.API modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Npgsql.EntityFrameworkCore.PostgreSQL should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Microsoft.EntityFrameworkCore.Tools should be updated from `8.0.8` to `9.0.8` (*recommended for .NET 9.0*)

#### HybridApp modifications

Project properties changes:
  - Target frameworks should be changed from `net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0-windows10.0.19041.0` to `net8.0-android;net8.0-ios;net8.0-maccatalyst;net8.0-windows10.0.19041.0;net9.0-windows`

NuGet packages changes:
  - Microsoft.Extensions.Http should be updated from `8.0.0` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.Extensions.Logging.Debug should be updated from `8.0.0` to `9.0.8` (*recommended for .NET 9.0*)

#### Ordering.UnitTests modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

#### Ordering.FunctionalTests modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Hosting.AppHost should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Aspire.Hosting.PostgreSQL should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Microsoft.AspNetCore.Mvc.Testing should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.AspNetCore.TestHost should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)

#### Catalog.FunctionalTests modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Hosting.AppHost should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Aspire.Hosting.PostgreSQL should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Microsoft.AspNetCore.Mvc.Testing should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.AspNetCore.TestHost should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)

#### Basket.UnitTests modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Microsoft.AspNetCore.Mvc.Testing should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)
  - Microsoft.Extensions.Identity.Stores should be updated from `8.0.7` to `9.0.8` (*recommended for .NET 9.0*)

#### eShop.AppHost modifications

Project properties changes:
  - Target framework should be changed from `net8.0` to `net9.0`

NuGet packages changes:
  - Aspire.Hosting.AppHost should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Aspire.Hosting.RabbitMQ should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Aspire.Hosting.Redis should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Aspire.Hosting.PostgreSQL should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)
  - Aspire.Hosting.Azure.CognitiveServices should be updated from `8.2.0` to `9.4.0` (*deprecated package - out of support*)