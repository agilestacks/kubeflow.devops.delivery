# Kubeflow

Kubeflow is an open, community driven project to make it easy to deploy and manage an ML stack on Kubernetes

The Kubeflow project is dedicated to making deployments of machine learning (ML) workflows on Kubernetes simple, portable and scalable. Our goal is not to recreate other services, but to provide a straightforward way to deploy best-of-breed open-source systems for ML to diverse infrastructures. Anywhere you are running Kubernetes, you should be able to run Kubeflow.

## Prerequisites

Before setting up Kubeflow you need to have a working Kubenretes cluser (supported versions: `v1.16` to `v1.21`). With enabled dynamic storage provisioner.

Don't have cluster? Don't worry we provide few templates that you can use as an examples for your clusters

1. [Google Kubernets Engine](#) - example of GKE cluster on GCP
2. Elastic Kubernetes Cluster (coming soon)

## Kubeflow Deployments

Choose one of the pre-built kubeflow templates

Kubeflow Stack | Description | Link
:--------------|:------------|:-----
|[Kubeflow on GKE](#) | Ready to deploy a kubeflow on empty GKE cluster. It will install ingress controller, istio and all Kubeflow components | <a href="https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:kubeflow-preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=composer-demo-app" rel="Open with Cloud Shell">![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)</a>

### Kubeflow Components

Kubeflow features full ML lifecycle for model training, huper parameter tuning and model serving. Most noticable components of Kubeflow you can find below

Component | Feature
:---------|:--------
[Notebooks](https://www.kubeflow.org/docs/components/notebooks/) | Jupyter notebook server 
[Pipelines](https://www.kubeflow.org/docs/components/pipelines/) | Provides a Python DSL for DAG to run distributed training 
[Katib](https://www.kubeflow.org/docs/components/katib/) | Hyper parameter tuning
[Tensorflow Training](https://www.kubeflow.org/docs/components/training/tftraining/) | Tensorflow training operator with `TFJob` custom resource
[Multi Tenancy](https://www.kubeflow.org/docs/components/multi-tenancy//) | Provides multi user isolation
[Central Dashboard](https://www.kubeflow.org/docs/components/central-dash/) | Common UI to access all Kubeflow applicaitons
[ML Metadata](https://www.kubeflow.org/docs/components/pipelines/concepts/metadata/) | Metadata store backed with relational database 
[Artifacts Store](https://www.kubeflow.org/docs/components/pipelines/concepts/output-artifact/) | Object store (such as Minio) to store results of the trainings

![kubeflow](https://github.com/IBM/KubeflowDojo/raw/master/images/kubeflow-dojo.png)


## See also:

* <https://kubeflow.org>
* <https://superhub.io>
