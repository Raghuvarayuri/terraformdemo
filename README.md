# devops-terragrunt
# terragrunt
A repo used to accompany devops-lecture-frontend and devops-lecture-backend and provision the infrastructure with Terragrunt and Terraform

## Requirements
@@ -81,9 +81,7 @@ Select Certificates & secrets. Click the New client secret button, then enter a

Navigate to the Subscriptions within the Azure Portal, then select the Subscription you wish to use, then click Access Control, and finally click Add, then click Add role assignment. Specify a Role Contributor will grant Read/Write on all resources in the Subscription for your service principal, then search and select the name of the Service Principal to assign it this role.

## Pipeline Stages

The CI/CD pipeline is divided into 3 stages: `Init`, `Plan` and `Apply`. 
The provision resources is divided into 3 stages: `Init`, `Plan` and `Apply`. 

In the `Init` stage we are creating the needed Azure resources for our terraform remote state. The purpose of the remote state is to keep track of changes and to have the ability to lock the state from concurrent changes. This stage will create for us a resource group and a storage account with a storage container. If any of the resources already exists, creation will be skipped.
