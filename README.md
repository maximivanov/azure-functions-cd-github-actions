# Continuous Deployment for Azure Functions with Github Actions

In VSCode you can use the Remote Containers extension to start the project in a Docker container.
It includes Node.js, Azure CLI, Terraform.

Login with `az cli`:

```bash
az login
```

Create cloud resources:

```bash
cd terraform
terraform init
terraform apply -var-file dev.tfvars # for dev env; replace with prod.tfvars for prod
```

Create a Repository Secret in the Github repo with the function app publish profile.

Trigger the `CD` workflow in the repo (via a commit or manually).

Function code will be deployed to the Function App in Azure.
