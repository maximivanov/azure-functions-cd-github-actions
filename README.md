# Continuous Deployment for Azure Functions with Github Actions

Deploy infra

```bash
cd terraform
terraform init
terraform apply
```

Create a Repository Secret in the Github repo with the function app publish profile.

Trigger the `CD` workflow in the repo.

Function code will be deployed to the Function App in Azure.
