# terraform-aws-ec2

This is a lightweight Terraform module that provisions a basic AWS EC2 instance. It is designed to be minimal, reusable, and easily extended for infrastructure-as-code (IaC) use cases on AWS.

## 📖 Description

The module creates a single EC2 instance using user-provided inputs for the AMI ID and instance type. It is intended for quick bootstrapping of compute resources in AWS and can be incorporated into larger Terraform configurations as a standalone component.

## ✅ Features

- Launches one EC2 instance
- Accepts custom AMI and instance type
- Easily pluggable into other Terraform projects
- AWS region is managed externally (e.g., via provider)

## 🔧 Inputs

| Variable         | Description                          | Type   | Required |
|------------------|--------------------------------------|--------|----------|
| `ami_id`         | The AMI ID to use for the instance   | string | ✅ Yes    |
| `instance_type`  | The type of EC2 instance to launch   | string | ✅ Yes    |

## 📂 Module Structure

- **`main.tf`** – Contains the resource definition for the EC2 instance.
- **`variables.tf`** – Defines the input variables required by the module.

## 🧱 Requirements

- Terraform CLI ≥ 1.0.0
- AWS Provider ≥ 5.0.0
- A valid AWS account and credentials (configured via environment or profile)

## 📝 Notes

- No default values are provided for the variables to enforce explicit configuration.
- This module does not handle networking, security groups, key pairs, or tags. These should be handled externally or by extending the module.

## 📄 License

This project is licensed under the MIT License.
