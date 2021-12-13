# Porter Bundle for Azure Service Operator

[![Bundle Build](https://github.com/Azure/azure-service-operator-porter/actions/workflows/main.yaml/badge.svg)](https://github.com/Azure/azure-service-operator-porter/actions/workflows/main.yaml)

Goal of this project is to create a Cloud Native Application Bundle (CNAB) using Porter which helps in deploying [Azure Service Operator](https://github.com/Azure/azure-service-operator).


## Prerequisite

User need to pre-install Porter. User will need the Porter binary on system PATH. Please download it from [Install Porter Page](https://porter.sh/install/).

 - 👉 To know more about Porter, please visit [Porter](https://porter.sh/).

## How to use it? 

Once current cluster context is set to the cluster in which user want to deploy Azure Service Operator. It takes simple 2 steps to deploy ASO with Porter.

1. Generate Credentials

Please follow [porter credential generate](https://porter.sh/cli/porter_credentials_generate/) to generate a named set of credentials for Porter. 

Helpful command which we used to generate credentials `porter credentials generate <cred-name> -–reference aksmcrimagescommon.azurecr.io/public/aks/porter/azure-service-operator:v0.0.1`


2. Deploy Azure Service Opertation (ASO) using bundle

Run command `porter install -c <cred-name> –-reference aksmcrimagescommon.azurecr.io/public/aks/porter/azure-service-operator:v0.0.1`

🧙‍♀️ Quick demo

![demo gif](resources/demo.gif)

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
