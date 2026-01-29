# Kubernetes Cluster Setup

This document explains the provisioning of the Kubernetes cluster using Terraform and AWS EKS.

## Components

- VPC with public and private subnets
- NAT Gateway
- EKS cluster
- Managed node groups

## Terraform Modules

- terraform-aws-modules/vpc/aws
- terraform-aws-modules/eks/aws

## Access

```bash
aws eks update-kubeconfig --region us-east-1 --name sre-observability-dev
kubectl get nodes
