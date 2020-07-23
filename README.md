# cdk-typescript-azurerm-k8s

Cloud Development Kit (CDK) TypeScript implementation to deploy Azure Kubernetes Service (AKS)

See the blog post [markwarneke.me]()

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

Run the `cdktf`

```bash
cdktf synth
cdktf diff
cdktf deploy
```