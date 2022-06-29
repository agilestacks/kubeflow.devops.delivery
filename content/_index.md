# Kubeflow

Kubeflow is a popular and flexible machin learning platform that you can run virtually on any Kubernetes cluster. This means almost anywhere. 

## Kubeflow Components

Kubeflow features full ML lifecycle for model training, huper parameter tuning and model serving. Most noticable components of Kubeflow you can find below

Component | Feature
:---------|:--------
[Notebooks](https://www.kubeflow.org/docs/components/notebooks/) | Notebook server. Provides: Jupyter Lab, R-Studio and Visual Studio Code IDE
[Pipelines](https://www.kubeflow.org/docs/components/pipelines/) | Provides a Python DSL for DAG to run distributed training 
[Katib](https://www.kubeflow.org/docs/components/katib/) | Hyper parameter tuning
[Tensorflow Training](https://www.kubeflow.org/docs/components/training/tftraining/) | Tensorflow training operator with `TFJob` custom resource
[Multi Tenancy](https://www.kubeflow.org/docs/components/multi-tenancy//) | Provides multi user isolation
[Central Dashboard](https://www.kubeflow.org/docs/components/central-dash/) | Common UI to access all Kubeflow applicaitons
[ML Metadata](https://www.kubeflow.org/docs/components/pipelines/concepts/metadata/) | Metadata store backed with relational database 
[Artifacts Store](https://www.kubeflow.org/docs/components/pipelines/concepts/output-artifact/) | Object store (such as Minio) to store results of the trainings
[KServe](http://kserve.github.io/) | Model serving engine from Kubeflow
[Seldon Core Operator](https://docs.seldon.io/projects/seldon-core/en/latest/charts/seldon-core-operator.html) | Provides Model serving with Seldon Core

![kubeflow](https://github.com/IBM/KubeflowDojo/raw/master/images/kubeflow-dojo.png)




# Kubeflow Deployments


We make it easy to deploy on your cluster by providing series of curated templates. 


Kubeflow Stack | Version | Description | Link
:--------------|:--------|:------------|:-----
|[Kubeflow on GKE](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp) | `v1.2` | Ready to deploy a kubeflow on empty GKE cluster. It will install ingress controller, istio and all Kubeflow components | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp)
|[Kubeflow on GKE](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:latest&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp) | `v1.5.1` | Ready to deploy a kubeflow on empty GKE cluster. It will install ingress controller, istio and all Kubeflow components | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&cloudshell_git_branch=v1.5.0&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:latest&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp)


## Prerequisites

Before setting up Kubeflow you need to have a working Kubenretes cluser (supported versions: `v1.16` to `v1.21`). With enabled dynamic storage provisioner.

Don't have cluster? Don't worry we provide few templates that you can use as an examples for your clusters

1. [Google Kubernets Engine](#) - example of GKE cluster on GCP
2. Elastic Kubernetes Cluster (coming soon)

## Kubeflow Deployments

Choose one of the pre-built kubeflow templates

Kubeflow Stack | Description | Link
:--------------|:------------|:-----
|[Kubeflow on GKE](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp) | Ready to deploy a kubeflow on empty GKE cluster. It will install ingress controller, istio and all Kubeflow components | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp)


## See also:

* <https://kubeflow.org>
* <https://superhub.io>
