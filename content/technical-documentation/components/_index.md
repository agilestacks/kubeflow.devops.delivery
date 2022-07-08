# Kubeflow Components

Kubeflow features full ML lifecycle for model training, huperparameter tuning and model serving. Most noticable components of Kubeflow you can find below.

| Component | Description |
| :---      | :---    |
| [Notebooks](notebooks) | Jupyter notebooks web application |
| [Pipelines](pipelines) | Provides a Python DSL for DAG to run distributed training |
| [Katib](katib) | Hyperparameter tuning |
| [TensorFlow Training](tensorflow-training) | Tensorflow training operator with `TFJob` custom resource |
| [Multi Tenancy](https://www.kubeflow.org/docs/components/multi-tenancy/) | Provides multi-user isolation |
| [Central Dashboard](central-dashboard) | Common UI to access all Kubeflow applicaitons |
| [ML Metadata](ml-metadata) | Metadata store backed with relational database |
| [Artifacts Store](https://www.kubeflow.org/docs/components/pipelines/concepts/output-artifact/) | Object store (such as Minio) to store results of the trainings |

The ASI Kubeflow distribution also includes components to extend or improve ML lifecycle.

| Component | Description |
| :---      | :---    |
| [Argo Workflows](argo-workflows) | Pipeline workflow engine |
| [Istio Ingress Gateway](istio-ingress-gateway) | |
| [Kubeflow Authn HTTP Filter](kubeflow-authn) | HTTP filter for Istio (Envoy) |
| [MinIO](minio) | Object storage |
