# .NET Core Conduit API Server

This codebase was created to demonstrate a fully fledged fullstack application built with ASP.NET Core (with Feature orientation) including CRUD operations, authentication, routing, pagination, and more.

We've gone to great lengths to adhere to the ASP.NET Core community styleguides & best practices.

# How it works

This is using ASP.NET Core with:

- CQRS and [MediatR](https://github.com/jbogard/MediatR)
  - [Simplifying Development and Separating Concerns with MediatR](https://blogs.msdn.microsoft.com/cdndevs/2016/01/26/simplifying-development-and-separating-concerns-with-mediatr/)
  - [CQRS with MediatR and AutoMapper](https://lostechies.com/jimmybogard/2015/05/05/cqrs-with-mediatr-and-automapper/)
  - [Thin Controllers with CQRS and MediatR](https://codeopinion.com/thin-controllers-cqrs-mediatr/)
- [AutoMapper](http://automapper.org)
- [Fluent Validation](https://github.com/JeremySkinner/FluentValidation)
- Feature folders and vertical slices
- [Entity Framework Core](https://docs.microsoft.com/en-us/ef/) on SQLite for demo purposes. Can easily be anything else EF Core supports. Open to porting to other ORMs/DBs.
- Built-in Swagger via [Swashbuckle.AspNetCore](https://github.com/domaindrivendev/Swashbuckle.AspNetCore)
- [Cake](http://cakebuild.net/) for building!
- JWT authentication using [ASP.NET Core JWT Bearer Authentication](https://github.com/aspnet/Security/tree/master/src/Microsoft.AspNetCore.Authentication.JwtBearer).

This basic architecture is based on this reference architecture: [https://github.com/jbogard/ContosoUniversityCore](https://github.com/jbogard/ContosoUniversityCore)

# Getting started

Install the .NET Core SDK and lots of documentation: [https://www.microsoft.com/net/download/core](https://www.microsoft.com/net/download/core)

Documentation for ASP.NET Core: [https://docs.microsoft.com/en-us/aspnet/core/](https://docs.microsoft.com/en-us/aspnet/core/)

## Docker Build

There is a 'Makefile' for OS X and Linux:

- `make build` executes `docker-compose build`
- `make run` executes `docker-compose run`

The above might work for Docker on Windows

## Local building

- Install Cake as a global tool: `dotnet tool install -g Cake.Tool`
- Run Cake: `dotnet cake build.cake`
  - Note: this publishes as an OS X runtime by default. Use the Cake argument `runtime` passing an RID explained here: https://docs.microsoft.com/en-us/dotnet/core/rid-catalog

## Swagger URL

- `http://localhost:5000/swagger`