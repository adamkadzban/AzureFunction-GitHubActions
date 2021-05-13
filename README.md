# AzureFunction-GitHubActions

A simple example of a .NET Azure Function that is built and deployed via GitHub Actions.

## Description

- ci.yml: Simple build to run on ever PR
- main.yml: Build and deploy to the "stage" slot on updates to 'main' branch

## Links

- Repository Actions: https://github.com/adamkadzban/AzureFunction-GitHubActions/actions
- Production HTTP Trigger: https://azurefunction-githubactions.azurewebsites.net/api/Function1
- Stage HTTP Trigger: https://azurefunction-githubactions-stage.azurewebsites.net/api/Function1