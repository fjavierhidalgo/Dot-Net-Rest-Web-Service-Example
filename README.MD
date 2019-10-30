# REST WEB SERVICE EXAMPLE IN .NET

Example exercise that publishes a service to consume through the Http protocol through its standardized request verbs.

In this exercise I would like to highlight a series of elements that have been included in the code and that I detail below:

### Layered Architecture

Simple software architecture in layers to decouple the domain and application of the technology used to perform the service. In the future, a new framework can be used without changing the core. In this way we look for scalability and ease in subsequent maintenance.

### HTTP protocol verbs

We can perform the necessary actions for the maintenance of the entities from any platform thanks to the HTTP protocol. The information exchange format is through the JSON standard.

### Dependency Injection

Dependency injection management using Autofac package installed from NuGet. In the code, the controller classes have been designed inheriting from a "base" class that will be common for all classes that will be included as an extension in the future.

### Asynchronous programming

The Get, Post, Put and Delete methods have been programmed with Async Task. With this we will allow them to be invoked by users asynchronously. Thus, its possible mass use is taken into account and in this way we avoid the unnecessary load of server resources.

### Control of Web Error

The code shows the example of the capture of error 404. An ApiController class has been included in the "Controllers / Infrastructure" folder for error handling.

## CONFIGURATION

In the Zip file is the complete solution in the absence of the "packages" folder that has not been included due to its large size.

Inside we have a SQL Server script to create the simple data structure (bd_DotNetEx.sql). Some sample records are included.

In the Web.config of the DNExMasterCRUD.WebAPI project and in App.config of the DNExMasterCRUD.Core project, the connection data referring to the server, user and password have been removed. To make the connection they would have to indicate the data of their connection.

Some NuGet packages have been included in the projects:

#### Include in DNExMasterCRUD.WebAPI:

Autofac.WebApi2 

Microsoft AspNet.WebApi.Cors

#### Include in DNExMasterCRUD.Core:

Microsoft.AspNet.WebApi.Client

Microsoft.AspNet.WebApi.Core
