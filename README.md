# Terraform EKS

Infrastructure as Code for provisioning an Amazon EKS cluster on AWS with Terraform.

## Overview

The project uses Terraform to define the infrastructure required for an Amazon EKS environment, including networking, IAM, security groups, the Kubernetes control plane, and worker node groups.

## Technologies

- Terraform
- AWS
- Amazon EKS
- Kubernetes
- kubectl
- AWS CLI

## Main components

- VPC and networking
- IAM roles and policies
- EKS cluster
- Worker node groups
- Security groups
- Terraform variables and outputs

## Deployment

```bash
aws configure
terraform init
terraform plan
terraform apply
```

After deployment, the Terraform outputs can be used to configure access to the cluster with `kubectl`.

To remove the infrastructure:

```bash
terraform destroy
```

This is a personal AWS/Kubernetes lab focused on learning EKS provisioning with Infrastructure as Code.
