# Kubeflow Stack on GCP

Here we explain how to deploy a Kubeflow into your Google Cloud Platform environment

## Deployment Prerequisites

* You should be signed in and have an active project in GCP: https://console.cloud.google.com
* You should have already deployed a GKE cluster. 
 
> Don't have a cluster? Not a problem. We have a GKE stack for you, follow this [link](#)

## Deployment 

### Deployment via Cloud Shell

The easiest way how to get started is via Cloud Shell Edititor. Choose from the list of available Kubeflow stacks

Kubeflow Stack | Description | Link
:--------------|:------------|:-----
Kubeflow cluster v1.2 | This is our latest Kubeflow stack available | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:kubeflow-preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp)

#### Start a new cloud shell session

What will happen when you click to the button:

1. You will start a new Cloud Shell editor session (best works with the Chrome Browser)
2. Cloud shell will use a Shellbox image with all tools needed to deploy a kubeflow. No additional configuration required, See [shellbox on gcr](gcr.io/superhub/cloud-shell:kubeflow-preview)
3. Cloud shell will clone a git repo with the stack files: See github repo: [kubeflow-stacks](https://github.com/agilestacks/kubeflow-stacks/tree/main/kubeflow-gcp)

#### Init stack

First you need initialize the sandbox configuration.
To do this please run the initialization command:

```bash
hub stack init
```

The command will:

1. Download the components described in `hub.yaml` 
2. Configure this Cloud Shell session for your GCP. It will ask other GCP essentials. It will take Region and Location (zone) from GCP metadat aserver.
3. You can change settings by modifying `.env` file

#### Configure and Deploy a stack

Once you are done with the configuration, use the following command to deploy the sandbox:

```bash
hub stack deploy
```

Before the first deployment you will be prompted for few questions. Your settings will be captured in `.env` file. 

1. Name of `GKE` cluster in your region. You will see a list of already deployed GKE clusters in your region. For different region, please adjust variables in `.env` file and thern run `hub stack deploy` command again
2. Name of the storage class (more info [here](https://kubernetes.io/docs/concepts/storage/storage-classes/)) GKE provides several storage classes you will see them 
3. Other questions... 

Once all configuration settings completed it will start the deployment automatically

#### Review configuration parameters before deployment

Wait, not so fast! I want to review coniguration settings (and possibly adjust) before the deployment.

In this case, run the following command

```bash
hub stack configure
```

This command will only do a configuration step and save results in `.env` file. So you can review and adjust. Once you are happy then run

```bash
hub stack deploy
```

## Clean Up

To remove your Kubeflow deployment, please run the following command

```
hub stack undeploy
```
