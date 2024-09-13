# AWS VPC with EC2 and RDS (Terraform)

This Terraform project sets up an AWS infrastructure with a Virtual Private Cloud (VPC) containing a public subnet and a private subnet. The public subnet hosts an EC2 instance, while the private subnet contains an RDS PostgreSQL instance. The EC2 instance can access the RDS instance through security groups, and the VPC is configured with an internet gateway for external access to the EC2 instance.

## Features

- **VPC**: Creates a Virtual Private Cloud with two subnets (public and private).
- **Subnets**:
  - Public subnet: Contains the EC2 instance.
  - Private subnet: Contains the RDS PostgreSQL instance.
- **EC2 Instance**: An Amazon Linux 2 EC2 instance is provisioned in the public subnet.
- **RDS PostgreSQL**: A PostgreSQL database is created in the private subnet.
- **Security Groups**:
  - One security group allows SSH access to the EC2 instance.
  - Another security group allows the EC2 instance to access the RDS instance on port 5432 (PostgreSQL).

## Prerequisites

- **Terraform**: [Install Terraform](https://www.terraform.io/downloads.html) (v0.12+ recommended).
- **AWS Account**: You need an AWS account with credentials configured (either via `~/.aws/credentials` or environment variables).
- **AWS CLI**: Optionally, [install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) to manage AWS resources.

## Setup Instructions

### 1. Clone the repository:

```bash
git clone <https://github.com/eshunemma/deploy-cpc-ec2-rds-terraform.git>
cd VPC-EC2-RDS
```
