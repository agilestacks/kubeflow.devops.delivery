# Getting Started

Here we provide tutorials on how to deploy Kubelfow on top of your Kubernetes clusters

## Prerequisites

Kubernetes version compatibility:

GKE with version between `v1.19` and `v1.21`

Following addons shoudl be enabled/disabled on your GKE cluster.

Addon | Description | Requirement
:--------------|:------------|:-----
`httpLoadBalancing` | This addon enables GCP native Ingress Controller for the GKE cluster. It will automatically provision desired firewall rules in reaction to `Ingress` resource. We are still testing compatibility to our essential components (`external-dns`, `cert-manager`). As of today this addon requires to provision certain resources in strict order. Otherwise expect some frustration. It is hard to recommend for us to use this addon. We recommaned to disable this addon. We also provide a component `nginx` as the replacement. | `disable`
`ConfigConnector` | Allows creation of GCP resources by submitting Kubernetes Custom Resources. Component `replikate` will react when new Kubeflow profile has been created and will deploy a GCP service account to give access to GCP to the pods deployed inside Kubeflow Profile | `enable`

Before deployment, `hub` will validate check on prerequisites above

> Here is a command to enable/disable addon in running GKE cluster

```bash
gcloud container clusters update \
  "my-gke-cluster" \
  --zone "my-gke-clyster-location" \ 
  --update-addons "HttpLoadBalancing=DISABLED,ConfigConnector=ENABLED"
```

### Don't know how to deploy GKE Cluster 

If you don't know how exactly to deploy GKE cluster that will fit Kubeflow rather well? Then proceed with this link. We have a GKE cluster template 

## Deploy Kubeflow 

### Deploy with Cloud Shell

[Cloud Shell Editor](https://cloud.google.com/shell/docs/editor-overview) is the _ephemeral_ container that runs in your GCP project. You can interact with this container via your Internet browser. This container runs from the Toolbox image provided by Agile Stacks. This image has curated list of tools required for successul deployment of kKubeflow

> Tip: you can create your own toolbox image with tools you want

## Choose Kubeflow Template

