# Exercise build
Improve the pipeline:
1. Give more readable names to the steps. So it's more clear what's happening in the build.
   - Hint: use displayname
1. Add unit tests as part of the build.
   - [Hint](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-test)
1. Introducing variables, in a seperate file or variable group
   - [Hint](https://learn.microsoft.com/en-us/azure/devops/pipelines/library/variable-groups)
1. Skip the Linux part by default, but can be configured with variables settable at queue time.
1. Add branch policy, add conditions to the pipeline that if a PR triggers the pipeline, the release part must be skipped.
   - [Hint](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/conditions)
1. By splitting the generic logic for builds to a template
   - [Hint](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/templates)
1. And store the template above in a seperate repo
   - [Hint](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/resources)
1. Pass a variable from Azure Keyvault
   - [Hint](https://thomasthornton.cloud/2021/06/24/storing-and-retrieving-secrets-in-azure-keyvault-with-variable-groups-in-azure-devops-pipelines/)
1. Implement caching for the packages
   - [Hint](https://learn.microsoft.com/en-us/azure/devops/pipelines/release/caching)
1. Installing the .net version is always part of the build. Skip this if it's already installed on the agent.
   - [Hint: list all installed dotnet sdks](https://learn.microsoft.com/en-us/dotnet/core/install/how-to-detect-installed-versions)
   - [Hint: define dynamically a variable in powershell](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/variables)
1. Build the application for multiple applications by applying `strategy` and `matrix` 
   - [Hint](https://docs.microsoft.com/en-us/azure/devops/pipelines/customize-pipeline#build-across-multiple-platforms)

# Exercise release
Improve the pipeline:
1. Add approvers to the different stages
1. By splitting the generic logic for releases to a template
   - [Hint](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/templates)
1. Split the multi-stage YAML pipeline in a seperate build en seperate release.
