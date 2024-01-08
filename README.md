#Example GitOps Deployment for Metabase

This repo contains Kubernetes manifests for creating a Metabase deployment with a Postgres DB, yaml configurations for creating these deployments as GitOps applications, as well as definition for a Codefresh pipeline that backs up the deployed database before updating the deployments.

####Repo Directories
#####db
Contains Kubernetes manifests for a PostgreSQL database deployment configured to work with the included Metabase deployment.
#####metabase
Contains Kubernetes manifests for a Metabase open source deployment configured to with with the included PostgreSQL DB deployment.
#####gitops-apps
Contains configuration yaml files for ArgoCD applications for PostgreSQL and Metabase, as they should appear in the application git source.
#####pipeline
Contains yaml file for a pipeline that backs up data in the DB before syncing and updating applications.