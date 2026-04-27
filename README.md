# .NET Delegate Pipeline

A .NET Web API demonstrating a delegate-based middleware pipeline pattern. Inspired by ASP.NET Core's request pipeline, it chains multiple handler delegates to process requests in sequence — useful for validation, transformation, and logging steps.

## Features

- Custom delegate pipeline (similar to ASP.NET Core middleware)
- DTO validation via pipeline handlers
- Repository pattern for data access
- ASP.NET MVC / Web API project

## Tech Stack

- C# / .NET Framework (ASP.NET MVC)
- NuGet packages

## Prerequisites

- [Visual Studio](https://visualstudio.microsoft.com/) 2019+ with ASP.NET workload, **or**
- [.NET SDK](https://dotnet.microsoft.com/download)

## Getting Started

### Using Visual Studio

1. Clone the repository:
   ```bash
   git clone https://github.com/ahasan09/dotnet-delegate-pipeline
   ```
2. Open `EcapPipeline/EcapPipeline.sln` in Visual Studio
3. Restore NuGet packages (right-click solution → **Restore NuGet Packages**)
4. Press **F5** to build and run

The API will start at `http://localhost:{port}` as configured in `Web.config`.

### Using .NET CLI

```bash
cd EcapPipeline
dotnet restore
dotnet build
dotnet run
```

## Project Structure

```
dotnet-delegate-pipeline/
├── EcapPipeline/           # Main Web API project
│   ├── Controllers/        # API controllers
│   ├── Handler/            # Pipeline delegate handlers
│   ├── Models/             # Domain models
│   ├── Validation/         # Validation handlers
│   └── Web.config          # App configuration
├── Dtos/                   # Data Transfer Objects
├── DtoValidation/          # DTO validation logic
├── Repository/             # Data repository layer
└── EcapPipeline.sln        # Visual Studio solution
```
