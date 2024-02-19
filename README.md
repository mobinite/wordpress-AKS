# Deploy Basic wordpress website to AKS

## Pre-requisite:
- Azure Subscription
- Create AKS cluster
- Installed Azure CLI and Kubectl

## Process:
- Connect to AKS Cluster in Terminal
- Run yaml using kubectl

### Connect to AKS Cluster
`az login`

#### Then check kubect
`kubectl version --client`

#### Set the AKS Cluster Subscription
`az account set --subscription ["Azure Subscription ID"]`

#### Download Cluster Credentials
`az aks get-credentials --resource-group ["Your Resource Group Name"] --name ["Your Cluster Name"] --overwrite-existing`

#### Start Deployment
- `kubectl get nodes`

![Alt text](Markdown/get%20nodes.png)

#### Modify your Kustomize file
![Alt text](Markdown/add%20password.png)


- `kubectl apply -k ./`
![Alt text](Markdown/Apply%20k.png)

- `kubectl get pods`
![Alt text](Markdown/get%20pods.png)
- `kubectl get svc`
![Alt text](Markdown/get%20svc.png)
- `kubectl get all`
![Alt text](Markdown/get%20all.png)


### Now browse the External IP
![Alt text](Markdown/wp%20installation%20done.png)
