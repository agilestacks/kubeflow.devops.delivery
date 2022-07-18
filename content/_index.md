# EPAM Kubeflow

## What is Kubeflow?

Kubeflow is an open, community driven project to make it easy to deploy and manage an ML stack on Kubernetes

The Kubeflow project is dedicated to making deployments of machine learning (ML) workflows on Kubernetes simple, portable and scalable. Our goal is not to recreate other services, but to provide a straightforward way to deploy best-of-breed open-source systems for ML to diverse infrastructures. Anywhere you are running Kubernetes, you should be able to run Kubeflow.

## EPAM Kubeflow distribution

The EPAM Kubeflow distribution provides additional important features and covers the typical needs of MLOps engineers and data scientists.

### Value of service

* We deliver an accurate, professional and ready to work, end-to-end ML platform
* Start free on your own or use our services for a professional quick start
* Competitive “Under-The-Radar” timeline & fixed price for the ‘Exploratory’ phase

### Tailor made ML platform

* Cover client's needs in both Engineering and Infrastructures aspects, reducing the client’s own engineering resources to a minimum
* Option to extend platform with data pipelines and CI/CD pipelines
* Step by step approach for any solution scale

### Training plans

* Available training plans, tailored for all ML practitioners, including scientists, engineers and infrastructure managers
* One-stop-shop Service for all components in your environment

### Base on Google's Kubeflow

* Our ML platform can run on any cloud / multi-cloud / on-prem / hybrid environments
* Open source – no license fees, Avoid vendor lock-in
* Well established, highly popular ML toolkit

### Cloud Agnostic deployment

Deploy to the existing client’s cloud provider with saving current benefits or prepare an optimal cloud resource plan for the client’s needs.

### Support Availability

* The client can choose to support the solution either by own team or with vendor services
* Professional support with optional access to EPAM’s ML experts

## Prerequisites

Before setting up Kubeflow you need to have a working Kubernetes cluster (supported versions: `v1.18` to `v1.21`). With enabled dynamic storage provisioner.

Don't have cluster? No problems - we provide a template that you can use as an example for your clusters:

* [Google Kubernets Engine](https://github.com/agilestacks/kubeflow-stacks/tree/main/examples/gke-cluster) - example of GKE cluster on GCP
* Elastic Kubernetes Cluster (coming soon)

## Kubeflow Deployments

Choose one of the pre-built kubeflow templates

| Kubeflow Stack | Description | Link |
| :---           | :---        | :--- |
| [Kubeflow on GKE](/getting-started/deploy-kubeflow-on-cloud/deploy-on-gke/) | Ready to deploy a kubeflow on empty GKE cluster. It will install ingress controller, istio and all Kubeflow components | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp) |

![kubeflow](https://github.com/IBM/KubeflowDojo/raw/master/images/kubeflow-dojo.png)

## See also

* <https://kubeflow.org>
* <https://superhub.io>
