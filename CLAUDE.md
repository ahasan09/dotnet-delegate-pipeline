# WebApiDelegate

ASP.NET MVC 5 / Web API 2 solution demonstrating the Delegate/Handler pipeline pattern for request validation and processing, using DTOs, a repository layer, and specification-based validation.

## Tech Stack
- C# / .NET Framework
- ASP.NET MVC 5 / Web API 2
- Visual Studio solution (.sln)
- NuGet (jQuery, Bootstrap, Application Insights)

## Project Structure
```
WebApiDelegate/
  EcapPipeline.sln
  EcapPipeline/          # Main Web API / MVC project
    Controllers/         # CustomerController, HomeController
    Handler/             # Request handler/pipeline classes
    Models/
    Validation/
  Dtos/                  # DTO class library
  Repository/            # Data access class library
  DtoValidation/         # DTO validation class library (CustomerSpecification)
  packages/              # NuGet restored packages
```

## Development
Open `EcapPipeline.sln` in Visual Studio (Windows) or JetBrains Rider, restore NuGet packages, then build and run (F5).

Key API endpoint prefix: `/api/customers`

## Key Notes
- .NET Framework project — requires Visual Studio on Windows or Rider.
- Implements a Chain-of-Responsibility-style handler pipeline for validating and processing Web API requests.
- NuGet packages are committed under the `packages/` directory.
