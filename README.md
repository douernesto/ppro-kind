# Kind Cluster and Kubernetes

Pipeline exampample that executes the following steps using Github Workflows and community runners and actions:

## To execute
1. Go to the project Actiona and trigger a manual Workflow Dispatch for "Kind Cluster Sample App"

## How it works

1. Checkout code
1. Create a Kind Cluster using GH Action
1. Install Kubectl using GH Action
1. Install Chainsaw using GH Action
    1. Chainsaw is a tool to make end to end testing Kubernetes operators entirely declarative.
1. Display Kubernetes Cluster Information
1. Create 2 namespaces
    1. "qa" and "prod", we will only use "qa"
1. Install an application using Helm, in this case "ingress-nginx"
1. Wait for "ingress-nginx" to be ready
1. Deploy a Sample Application using manifests
    1. Create "Deployment"
    1. Create "Service"
    1. Create "Ingress"
1. List Kubernetes resources on the cluster
1. Run Chainsaw Tests
    1. A very simple deployment of a configmap manifest