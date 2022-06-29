# Deploy Kubeflow on GKE cluster

Here we describe how to deploy Kubeflow on GKE

## Prerquisites

To deploy a GKE feel free to follow this manual. 

## GKE Addons

Following addons shoudl be enabled/disabled on your GKE cluster.

Addon | Description | Requirement
:--------------|:------------|:-----
`httpLoadBalancing` | We recommend to deploy `nginx` as an Iingress cotroller instead. | `disable`
`ConfigConnector` | For GCP access by creating a GCP Service Account and linked to Kubeflow Profile | `enable`

To update addons you can use command below

```bash
gcloud container clusters update \
  "my-gke-cluster" \
  --zone "my-gke-clyster-location" \ 
  --update-addons "HttpLoadBalancing=DISABLED,ConfigConnector=ENABLED"
```

## Choose deployment option

Proceed with desired deployment type

* Deploy using [Cloud Shell](./deploy-gcp-cloudshell.md)
* Deploy using [tools on your workstation](./deploy-gcp-cloudshell.md)

