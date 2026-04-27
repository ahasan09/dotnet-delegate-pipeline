# Improvement Plan: WebApiDelegate

## Overview
.NET Framework 4.x Web API project demonstrating the handler pipeline pattern. Requires Windows/Visual Studio. No unit tests, no OpenAPI documentation, no containerization.

## Improvements

### Modernization (High Priority)
- Migrate from .NET Framework to .NET 9 (current LTS, cross-platform, actively supported)
- Migrate from Web API 2 to ASP.NET Core minimal APIs or controllers
- Replace `packages/` committed NuGet packages with a standard `PackageReference` restore (remove the `packages/` folder from the repo)

### Testing
- Add xUnit unit tests for each handler in the pipeline, testing both happy path and validation failure cases
- Add integration tests using `WebApplicationFactory<T>` (ASP.NET Core test host)
- Target ≥80% code coverage

### API Documentation
- Add Swagger/OpenAPI docs via `Swashbuckle.AspNetCore`
- Document all request/response DTOs with XML comments

### Code Quality
- Enable nullable reference types and `<TreatWarningsAsErrors>true</TreatWarningsAsErrors>`
- Add `.editorconfig` + `dotnet format` for consistent code style
- Add FluentValidation to replace the manual `CustomerSpecification` pattern, or document the specification pattern clearly

### Security
- Add API key or JWT authentication to the `/api/customers` endpoint
- Add input length limits and sanitization in the validation pipeline
- Rotate any secrets out of `Web.config` into environment variables / `appsettings.json`

### DevOps
- Add a `Dockerfile` for containerized deployment
- Add GitHub Actions CI: build + test + publish on every PR
- Add a `docker-compose.yml` for local development
