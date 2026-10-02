# Terraform EKS

A Terraform learning project focused on provisioning Amazon EKS infrastructure on AWS.

## Scope

The repository is dedicated to practicing the Infrastructure as Code workflow for Kubernetes on AWS.

```text
Terraform configuration
        |
        v
terraform plan
        |
        v
terraform apply
        |
        v
AWS / EKS
        |
        v
kubectl
```

## Technologies

- Terraform
- AWS
- Amazon EKS
- Kubernetes
- kubectl
- AWS CLI

## Workflow

```bash
aws configure
terraform init
terraform validate
terraform plan
terraform apply
```

After provisioning, Kubernetes access can be configured with the AWS CLI and verified with:

```bash
kubectl get nodes
```

Remove the provisioned resources with:

```bash
terraform destroy
```

This is a personal Cloud/DevOps lab for practicing EKS provisioning and Infrastructure as Code.
