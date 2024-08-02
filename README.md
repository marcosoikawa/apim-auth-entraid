---
ArtifactType: website
Language: C#
Platform: Windows
Tags: Azure, EntraID, API Management
---

# API Authentication with API Management (APIM) and Entra ID using Polcies 

![GitHub](https://img.shields.io/github/license/marcosoikawa/apim-auth-entraid) 
![GitHub repo size](https://img.shields.io/github/repo-size/marcosoikawa/apim-auth-entraid) 
[![Azure](https://badgen.net/badge/icon/azure?icon=azure&label)](https://azure.microsoft.com)

![GitHub last commit](https://img.shields.io/github/last-commit/marcosoikawa/apim-auth-entraid)
![GitHub top language](https://img.shields.io/github/languages/top/marcosoikawa/apim-auth-entraid)


## Scenario

The main objective of this LAB is to demonstrate how Azure API Management (APIM) can centralized authentication and authorizaton of APIs using Entra ID using APIM Policy (validate-jwt) and App Roles of Entra ID. This is very usefull when you have legacy APIs, APIs with no OAuth 2.0 / OIDC or even if you need to centralized management of authentication and authentication in one single pane of glass
![Topology](./media/architecture1.png)

# Prerequisites

- An Azure account with an active subscription. [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).

## Create Environment

Variable block
```bash
let "randomIdentifier=$RANDOM"
resourceGroup="apim-auth"
apim="apim-auth-$randomIdentifier"
```

Create Resource Group
```bash
az group create \
    --name $resourceGroup \
    --location brazilsouth
```

Ceate an API Management
```bash
az apim create --name $apim --resource-group $resourceGroup \
  --publisher-name Contoso --publisher-email admin@contoso.com \
  --no-wait
```
## Next steps


## Learn more

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

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.