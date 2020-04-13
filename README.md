---
languages:
- csharp
- aspx-csharp
page_type: sample
description: "This is a sample application that you can use to follow along with the Run a RESTful API with CORS in Azure App Service tutorial."
products:
- azure
- aspnet-core
- azure-app-service
---

# ASP.NET Core API sample for Azure App Service

This is a sample application that you can use to follow along with the tutorial at 
[Run a RESTful API with CORS in Azure App Service](https://docs.microsoft.com/azure/app-service/app-service-web-tutorial-rest-api). 

## License

See [LICENSE](https://github.com/Azure-Samples/dotnet-core-api/blob/master/LICENSE.md).

## Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
  
az group create --name myAuthApiApp --location "East US"
az appservice plan create --name myAuthAppServicePlan --resource-group myAuthApiApp --sku FREE
az webapp create --resource-group DotNetSqlApp --plan myDotNetSqlApp --name ApiFrontEnd11 --deployment-local-git --query deploymentLocalGitUrl
az webapp create --resource-group DotNetSqlApp --plan myDotNetSqlApp --name ApiBackEnd11 --deployment-local-git --query deploymentLocalGitUrl

"https://jwilkadmin23@apifrontend11.scm.azurewebsites.net/ApiFrontEnd11.git"
"https://jwilkadmin23@apibackend11.scm.azurewebsites.net/ApiBackEnd11.git"

https://docs.microsoft.com/en-us/azure/app-service/app-service-web-tutorial-auth-aad

Backend App - http://ApiBackEnd11.azurewebsites.net
FrontEndApp - http://ApiFrontEnd11.azurewebsites.net


git remote add frontend "https://jwilkadmin23@apifrontend11.scm.azurewebsites.net:443/ApiFrontEnd11.git"
git push frontend master

git remote add backend "https://jwilkadmin23@apibackend11.scm.azurewebsites.net:443/ApiBackEnd11.git"
git push backend master

--user-name jwilkadmin23 --password R3l3ntl3ss