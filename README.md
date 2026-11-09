dotnet-sdk
Introduction

dotnet-sdk is the software development kit for building, compiling, testing, and publishing applications with the .NET platform. It provides developers with the essential command-line tools, compilers, build infrastructure, and project management capabilities required to develop modern applications using C#, F#, and Visual Basic. The .NET SDK supports multiple application types, including console applications, web services, REST APIs, background services, class libraries, and cross-platform solutions.

The primary component of the SDK is the .NET Command-Line Interface (CLI), which allows developers to manage the entire application development lifecycle directly from a terminal. Using the dotnet command, IT professionals can create projects, restore NuGet dependencies, compile source code, execute automated tests, and generate deployment-ready packages. These operations can be integrated into development scripts, automated build systems, and continuous integration and continuous delivery (CI/CD) pipelines.

The SDK also includes the MSBuild build engine, language compilers, project templates, and tools for managing .NET workloads. This infrastructure enables consistent project configuration and reproducible builds across Windows, Linux, and macOS environments. Developers can target different .NET versions and application frameworks while maintaining a unified development workflow.

dotnet-sdk is particularly useful for software engineers, DevOps specialists, system administrators, and development teams responsible for maintaining .NET applications. It supports local development, automated compilation, application testing, containerized deployment, and production publishing. Whether configuring a development workstation or preparing a build environment on a server, the SDK provides the core tooling needed to manage .NET projects efficiently from source code to executable application.

Installing and Configuring the .NET SDK

Installing dotnet-sdk is the first step in preparing an environment for .NET application development. The SDK can be installed on Windows, Linux, and macOS using platform-specific installation packages, package managers, or official installation scripts. Linux distributions may also provide version-specific packages through their repositories, allowing administrators to install and maintain the development environment using standard system package management tools.

After installation, verify that the command-line tools are available by executing:

bash
dotnet --version


This command displays the active SDK version. To inspect the installed SDKs and available runtime versions, use:

bash
dotnet --list-sdks
dotnet --list-runtimes
dotnet --info


The dotnet --info command is especially useful for troubleshooting because it displays the SDK installation path, operating system information, architecture, and environment configuration.

Developers can create a new project using built-in templates. For example, the following commands initialize and run a basic console application:

bash
dotnet new console -n SampleApp
cd SampleApp
dotnet run


For reproducible development environments, a global.json file can specify which SDK version a project or repository should use. This is particularly important when several SDK versions are installed on the same machine or when build environments must remain consistent across development and CI/CD systems.

Building, Testing, and Publishing .NET Applications

The .NET SDK provides an integrated command-line workflow for compiling applications, managing dependencies, running automated tests, and preparing production deployments. These operations are available through the dotnet CLI and can be executed individually or combined into automated development pipelines.

Dependency management is handled through NuGet. Before compilation, restore project dependencies with:

bash
dotnet restore


To compile a project and generate its build artifacts, execute:

bash
dotnet build


During development, applications can be launched directly using dotnet run. This command builds the project when necessary and starts the application. For automated quality assurance, developers can use dotnet test to execute configured unit and integration test projects. Test results can then be incorporated into CI/CD workflows to identify compilation errors and regressions before deployment.

Publishing prepares an application for distribution or production execution. For example:

bash
dotnet publish -c Release -o ./publish


The Release configuration enables production-oriented build settings, while the output directory contains the published application files. Developers can also specify a target framework and runtime identifier to control deployment compatibility. For example, -r linux-x64 targets a 64-bit Linux environment.

The SDK supports framework-dependent and self-contained publishing models. Framework-dependent deployments require a compatible .NET runtime on the destination system, whereas self-contained deployments include the required runtime components. Single-file publishing is another available deployment option when configured appropriately.

These capabilities make dotnet-sdk suitable for automated builds, server-side application development, container image preparation, and repeatable software releases. IT teams can use the same CLI commands in local environments and build agents to standardize compilation, testing, and application deployment processes.
