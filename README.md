# cdk-typescript-azurerm-k8s

Cloud Development Kit (CDK) TypeScript implementation to deploy Azure Kubernetes Service (AKS)

See the blog post [markwarneke.me](https://markwarneke.me/2020-07-23-Deploy-AKS-Kubernetes-Using-TypeScript-Terraform-CDK/)

## Prerequisites

- install [azure-cli](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)
- install [cdktf-cli](https://learn.hashicorp.com/terraform/cdktf/cdktf-install)

## Running

Install the dependency providers from [`cdktf.json`](cdktf.json).

```json
{
  "language": "typescript",
  "app": "npm run --silent compile && node main.js",
  "terraformProviders": [
    "azurerm@~> 2.0.0"
  ]
}
```

```bash
cdktf get
```

Export the used service principal in environment variables as environment variables

```bash
export AZ_SP_CLIENT_ID=''
export AZ_SP_CLIENT_SECRET=''`
```

Run the `cdktf`

```bash
cdktf synth
cdktf diff
cdktf deploy
```
