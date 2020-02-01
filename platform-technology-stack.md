README.md
Platform Technology Stack

Layer Tech Purpose Reference UI Angular 2 UI Framework https://angular.io  UI TypeScript JavaScript https://www.typescriptlang.org/docs/index.html  UI RxJs Reactive programming http://reactivex.io/rxjs/manual/overview.html  UI SCSS CSS preprocessor https://www.npmjs.com/package/scss  UI HTML5 Browser layout language https://www.w3schools.com/html/html5_intro.asp  Web API ASP.NET  Web API 4.6.2 Web service platform https://www.asp.net/web-api/overview  Web API Autofac Dependency Injection https://autofac.org/  Web API Owin/Katana Hosting Framework https://www.asp.net/aspnet/overview/owin-and-katana  Storage SQL Server 2016 Persistence https://msdn.microsoft.com/en-us/library/ms130214.aspx 

Developer Tools

Tool Purpose Vendor Visual Studio 2015 .NET Development Microsoft ReSharper .NET Development JetBrains VSCode Front-End Development Microsoft Beyond Compare Diff/Merge Scooter Software NodeJs LTS Javascript Engine for Angular 2, SASS, TypeScript, etc. NodeJS Angular-CLI Command-line interface for Angular development Google (Angular) SQL Server Data Tools Developer Tools for SQL Server Microsoft

Environments

The project supports several different environments including Dev, QA, Stage, and Production.

Developing with Git

We use Git as our source control repository. See below for Git configuration and branching strategy:

Initialize Git Configuration Git Branching Strategy Test Development Strategy

All development will include automated testing to validate proper functioning. Guidance on automated test development is here.

Web API Guidance

This project creates a web API using these standards and conventions that provide back end support to our clients.

Deployments

When creating a deployment package, follow this packaging guidance.

Angular 2

Change Detection

For large components, you should consider using the OnPush change detection strategy in Angular. This requires working in a new pattern and using other tools available.

http://blog.thoughtram.io/angular/2016/02/22/angular-2-change-detection-explained.html  http://blog.angular-university.io/how-does-angular-2-change-detection-really-work/  Other Resources

C# Naming Guidelines Angular Architecture Angular Transclusion Angular Material Design Lite Git Branching Model BEM Intro BEM Documentation
