# Terraform Module to provision Krateo on a GKE Cluster

This repo is a fork of [Learn Terraform - Provision a GKE Cluster repository](https://github.com/hashicorp/learn-terraform-provision-gke-cluster) related to the [Provision a GKE Cluster tutorial](https://developer.hashicorp.com/terraform/tutorials/kubernetes/gke), containing Terraform configuration files to provision an GKE cluster on GCP.

This sample repo also creates a VPC and subnet for the GKE cluster. This is not
required but highly recommended to keep your GKE cluster isolated.

## Install

Authorize the SDK to access GCP using your user account credentials and add the SDK to your PATH. This steps requires you to login and select the project you want to work in.
```console
$ gcloud init
```

Add your account to the Application Default Credentials (ADC). This will allow Terraform to access these credentials to provision resources on GCloud:
```console
$ gcloud auth application-default login
```

Enable container service:
```console
$ gcloud services enable container
```

Apply Terraform configuration with your tfvars file:
```console
$ terraform apply -var-file="temp.tfvars"
```