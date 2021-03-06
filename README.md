# AzureFunction-GitHubActions

A simple example of a .NET Azure Function that is built and deployed via GitHub Actions.

## Description

- ci.yml: Simple build to run on ever PR
- main.yml: Build and deploy to the "stage" slot on updates to 'main' branch
- manual.yml: Swap slots

The Azure Function App was initially set up via the Portal. A GitHub Secret contains the RBAC Service Principal that these workflows use to log in to Azure.

## Builds

There are no build scripts. It might be worth adding them as a POC. Just run ```dotnet build --configuration Release --output ./output``` from the project folder. 

## Deployments

Builds on the `main` branch automatically deploy to the `stage` slot. This is done using the [Azure Functions Action](https://github.com/marketplace/actions/azure-functions-action).

More information about this Action's parameters is available [here](https://github.com/marketplace/actions/azure-functions-action#github-action-parameters).

## Links

- Repository Actions: https://github.com/adamkadzban/AzureFunction-GitHubActions/actions
- Production HTTP Trigger: https://azurefunction-githubactions.azurewebsites.net/api/Function1
- Stage HTTP Trigger: https://azurefunction-githubactions-stage.azurewebsites.net/api/Function1