## Deploy with Cloud Shell

This is probably the easiest way how to deploy Kubeflow. You don't need to install any automation tool. When you run a Cloud Shell session it will execute a Toolbox image with all tools required

## Prerequisites

* Use curated, pre-built image [`gcr.io/superhub/cloud-shell`](https://gcr.io/superhub/cloud-shell) to run your cloud shell.

> See dockerfile on the Github: [agilestacks/toolbox](https://github.com/agilestacks/toolbox/tree/master/gcp-cloud-shell)

## Deploy Kubeflow

### Choose Kubeflow Template

Select one of the following templatesand start the new cloud shell session

Kubeflow Stack | Description | Link
:--------------|:------------|:-----
Kubeflow cluster `v1.5.1` | This is our latest Kubeflow stack available | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:kubeflow-preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp)
Kubeflow cluster `v1.2.0`| Previous version of our Kubeflow Stack | [![CloudShell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://ssh.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/agilestacks/kubeflow-stacks&&cloudshell_git_branch=main&cloudshell_image=gcr.io/superhub/cloud-shell:kubeflow-preview&cloudshell_open_in_editor=hub.yaml&cloudshell_workspace=kubeflow-gcp)

> NOTE: these templates has been available on Github: [agilestacks/kubeflow-stacks](https://github.com/agilestacks/kubeflow-stacks/tree/main/kubeflow-gcp)

### Deploy TLDR

```bash
hub stack init
hub stack deploy
hub show -q '.outputs.kubeflow.url'
# https://kubeflow.example.com
```

Following chapters will exmplain with a bit more details what is going on

### Initialize Stack

You will be prompted to trust to the image and github repository.

Run the following command 

```bash
hub stack init
```

This command wil
1. Prompt you to select GCP project and location
2. Download source code of the components listed in `hub.yaml` file

### Deploy Kubeflow

```bash
hub stack deploy
```

Or; if you want to review configuration stored in `.env` file. then run following command.

```bash
hub stack configure
# review configuration stored in .env file
hub stack deploy
```

### Observing deployment results

Once Kubeflow has been been deployed you can confirm it by running followng command 

```bash
hub show
# ...
# status: deployed
```

To observe kubeflow URL: 

```bash
hub show -q ".outputs.kubeflow.url"
# https://kubreflow.example.com
```

> Note: you can apply filter query to the results in the `jq` style.

## To remove Kubeflow

There is a command reversive to deployment: `undeploy`

### Undeploy TLDR

TLDR command would look like 

```bash
hub stack undeploy
hub show -q ".status"
# status: undeployed
hub stack rm
```

> Note: this will not delete Kubernetes cluster. Cluster level resources such as CRDs and namespaces will remain as well as it may contain user data.

## See Also

