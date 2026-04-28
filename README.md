# Terraform EKS

Infrastructure as Code for provisioning Amazon EKS (Elastic Kubernetes Service) clusters on AWS using Terraform.

## 📋 Description

This repository contains Terraform configurations for setting up and managing production-ready EKS clusters on AWS. It includes configurations for networking, security groups, IAM roles, node groups, and cluster management.

## 🛠️ Tech Stack

- **Infrastructure as Code:** Terraform (HCL)
- **Cloud Provider:** AWS
- **Container Orchestration:** Kubernetes (EKS)
- **Version Control:** Git

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Terraform >= 1.0
- AWS CLI configured with appropriate credentials
- kubectl >= 1.24
- helm (optional, for package management)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Marcin4356/Terraform_EKS.git
cd Terraform_EKS
```

### 2. Configure AWS Credentials

```bash
aws configure
```

### 3. Initialize Terraform

```bash
terraform init
```

### 4. Review the Plan

```bash
terraform plan
```

### 5. Apply Configuration

```bash
terraform apply
```

## 📁 Project Structure

```
Terraform_EKS/
├── main.tf              # Main Terraform configuration
├── variables.tf         # Input variables
├── outputs.tf           # Output values
├── vpc.tf              # VPC and networking setup
├── iam.tf              # IAM roles and policies
├── eks-cluster.tf      # EKS cluster configuration
├── node-groups.tf      # Worker node groups
├── security.tf         # Security groups
├── terraform.tfvars    # Terraform variables (copy from .example)
└── README.md           # This file
```

## 🔧 Configuration

Update `terraform.tfvars` with your desired values:

```hcl
aws_region             = "eu-central-1"
cluster_name           = "my-eks-cluster"
cluster_version        = "1.27"
node_group_min_size    = 1
node_group_max_size    = 5
instance_types         = ["t3.medium"]
```

## 📝 Outputs

After applying the configuration, Terraform will output:

- Cluster endpoint
- Cluster security group ID
- Node group IDs
- IAM role ARNs

## 🧹 Cleanup

To destroy all resources:

```bash
terraform destroy
```

## 📚 Resources

- [AWS EKS Documentation](https://docs.aws.amazon.com/eks/)
- [Terraform AWS Provider](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)
- [Kubernetes Documentation](https://kubernetes.io/docs/)

## 📝 License

This project is open source and available under the MIT License.

## 👤 Author

**Marcin4356** - [GitHub Profile](https://github.com/Marcin4356)

---

*Last updated: 2026-04-28*
