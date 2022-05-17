---
title: Kubeflow
---

Kubeflow has been available via stacks of components. At present there is only one stack (for GCP), yet more will come in the near future. 

## Deployment Prerequisites

* You should be signed in and have an active project in GCP: https://console.cloud.google.com
* You should have already deployed a GKE cluster
 
> Note: there is a separate stack for GKE. It can act as an example, please feel free to customize the stack and deploy it: [link](#)

## Quick Start

Choose a kubeflow template and run a cloud shell session.

```bash
hub stack init
hub stack deploy
```

Or the following, if you want to review settings before deployment.

```bash
hub stack init
hub stack configure
hub stack deploy
```

List of pre-built Kubeflow stacks deployable via GCP Cloud Shell.

Kubeflow Stack | Description | Link
:--------------|:------------|:-----
Kubeflow cluster v1.2 | This is our latest Kubeflow stack available | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:kubeflow-preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp)

## Under the Hood 

### Cloud Shell Editor

[Cloud Shell Editor](https://cloud.google.com/shell/docs/editor-overview) is the _ephemeral_ container that runs in your GCP project. You can access it via your Internet browser. You will also see a VSCode, as a convinient way to review configuration and modify stack and it's components if needed. Basically you can use VSCode as your DevOps IDE.

Use terminal for deployment: we use [hub cli](superhub.io) as a a single deployment tool that can switch between different deployment tools, native to each individual component and pass input and output parameters between them.

Each Cloud Shell session will use a special *Toolbox* Image optimized to run as a Cloud Shell Editor container. It contains all necessary and pre-tested tools to execute Kubeflow deployment. 

* Toolbox content can be found here: https://github.com/agilestacks/toolbox/tree/google/gcp-cloud-shell
* Pulled from GCR registry: [gcr.io/superhub/cloud-shell](https://gcr.io/superhub/cloud-shell:kubeflow-preview)

Primary tools used during the deployment:

* `gcloud`
* `kubectl` (with kustomze `v4.0+`)
* `helm`
* `git`

### What happens during the deployment

When you run a `hub stack init` Then `hub` will read a components described in `hub.yaml` file and download it. It will also prompt for GCP project. There are number of `hub extensions` (plugins) primarilly written in shell. You will find it in `hub.yaml` in the section called `extensions`

When you run `hub stack configure` (or implicitly during `hub stack deploy`), then `gcp` extension will generate a new domain name and store it in the form of `HUB_DOMAIN_NAME` variable. Actually all variables has been pased to the `hub.yaml` via `.env` file. You don't want to put your `.env` file in the git. 

This domain name will be used by the `hub` as a natural ID of your deployment. If you have your own domain available as a DNS zone in GCP, then you can refer it via `hub stack configure --domain-name kubeflow.example.com`. 

TLS is a required by Kubeflow. Every deployment has been backed by `Lets Encrypt` certificate. 
