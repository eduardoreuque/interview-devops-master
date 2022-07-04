# Docker image for the build environment
FROM mcr.microsoft.com/dotnet/core/sdk:2.2.207 AS base

# Docker image for the runtime environment
FROM mcr.microsoft.com/dotnet/core/aspnet:2.2.8

# This command starts up the app
ENTRYPOINT ["dotnet", "Conduit.dll"]