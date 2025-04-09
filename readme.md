to Create a helm chart
> helm create cloud-run

Generate the yaml to be used

> helm template cloud-run ./ -f values_geral.yaml -f values_specific.yaml > service.yaml

Authenticate to google cloud using gcloud

> gcloud auth login

Replace the cloud run

> gcloud run services replace service.yaml --project_id=$Project_ID

Based on [Leveraging Helm for Cloud Run deployments on Google Cloud Platform](https://medium.com/@dr.daler.boboev/leveraging-helm-for-cloud-run-deployments-on-google-cloud-platform-fc044438f2ce)
