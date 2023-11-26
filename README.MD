# SoftIssue-Core

## Description
SoftIssue-Core is a .NET 8 solution designed for building scalable web applications with a microservices architecture. The solution includes a WebAPI project for backend controllers, microservices in the Services directory, and a shared library for common functionalities.

### Project Structure
- **SoftIssue-Core/SoftIssue.sln**: The main solution file.
- **SoftIssue-Core/SoftIssueApi**: The WebAPI project for backend controllers.
- **SoftIssue-Core/Services/MyService**: Microservices projects.
- **SoftIssue-Core/SharedLibrary**: Shared library for common code.

## Prerequisites
- .NET 8 SDK
- VS Code, Rider, Visual Studio 2022 or a similar IDE that supports .NET 8

## Getting Started

### Clone the Repository
To get started, clone the repository to your local machine.
### Building the Solution
Navigate to the solution directory and build the solution:

```bash
git clone [repository-url]
```

```bash
cd SoftIssue-Core
dotnet build
```
### Running the WebAPI
To run the WebAPI project:

```bash
cd SoftIssueApi
dotnet run
```
### Accessing Swagger UI
Once the WebAPI project is running, you can access the Swagger UI to interact with the API by navigating to http://localhost:5000/swagger in your web browser.

### Adding a New Service
To add a new service:

#### Create a new project in the Services directory.
Add the new project to the solution file:
```bash
dotnet sln SoftIssue.sln add ./Services/NewService/NewService.csproj
```
#### Reference the SharedLibrary if needed:
```bash
dotnet add ./Services/NewService/NewService.csproj reference ./SharedLibrary/SharedLibrary.csproj
```
### Managing NuGet Packages
Adding a NuGet Package:
```bash
Copy code
dotnet add package [package-name]
```
### Restoring NuGet Packages:
```bash
Copy code
dotnet restore
```
## Contributing
Contributions to SoftIssue-Core are welcome. Please ensure you follow the coding standards and write necessary tests for new features.