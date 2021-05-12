# FuncExamples
Several dotnet core and dotnet 5 examples of functions triggered based on EventHubs, REST and Timer events.  These examples are based heavily on existing Microsoft docs however simply consolidated into a single repo to ease sharing with customers.  

## Prerequisites
- **DotNet 5 SDK** - Have the [dotnet 5 SDK](https://dotnet.microsoft.com/download/dotnet/5.0) downloaded and installed
- **Function Core (CLI) Tools** - Have the Function Core Tools v3+ downloaded and isntalled by following the instructions in the following repo: https://github.com/Azure/azure-functions-core-tools
- **Azure Storage Emulator (or Azurite)** - Functions require Azure Storage (or an emulated Azure Storage) in order to run and log data.  This requires the development machine to have either the Azure Storage Emulator or the Azurite Emulator installed.  Azure Storage Emulator comes as a part of the [Azure SDK](https://azure.microsoft.com/en-us/downloads/), but Azurite can be installed within VSCode as described [here](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azurite).  

## Building & Running Code
In order to run the source code in this repo locally in a development environment, a `local.settings.json` file must be added with a valid event hub connecction string provided for `Values:ehConnection`.  A sample file has been provided in this repo but renamed to  `example_local.settings.json` and can be used as a starting point if just renamed to remove `example_`.  

This is a way (similar to `dotnet user-secrets`) that the Azure Functions SDK offers to add local secret values/settings without having them accidentally checking them into source control and sharing them accidentally. 

As with any Function, to test them locally, simply run the following command line `func host start --functions myFunctionToRun`.  For more on building and testing dotnet functions, please refer to the documentation here: https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local 
