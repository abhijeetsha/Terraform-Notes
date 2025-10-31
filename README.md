# Terraform-Notes
## 🌍 What is Terraform?
### Ans:- Terraform is an open-source Infrastructure as Code (IaC) tool developed by HashiCorp.
It is used to automate the creation, management, and destruction of cloud infrastructure — such as AWS, Azure, GCP, and others — using simple configuration files.

## ⚙️ Simple Definition:
### Ans: Terraform allows you to define your cloud infrastructure as code in .tf files, and then it creates or updates the actual infrastructure automatically.

## 🧱 Key Concepts in Terraform
### Ans: Concepts:- 
* Provider	>>>>>>> Plugin that interacts with a cloud service (e.g., AWS, Azure, GCP)
* Resource	>>>>>>> A piece of infrastructure (e.g., EC2 instance, S3 bucket, etc.)
* Variable	>>>>> Input values used in configuration files
* State File (terraform.tfstate)	>>>>>>>> Tracks the current state of your infrastructure
* Module	>>>>>>> A reusable set of Terraform configuration files
* Plan	>>>>>>>> Shows what Terraform will do before applying changes

## 🗂️ Terraform Workflow (Lifecycle)
### Ans: 
* Write — Define infrastructure in .tf files.
* Init — Initialize the working directory and download provider plugins.
* Plan — Preview changes before applying them.
* Apply — Execute the plan and create/update resources.
* Destroy — Delete all resources defined in Terraform.

## 🧰 Basic Terraform Commands:-
### Ans: 
* terraform init >>>>> Initialize Terraform
* terraform validate >>>>> Validate Configuration
* terraform plan >>>>>> View the Execution Plan
* terraform apply >>>>>>> Apply the Configuration
* terraform show >>>>>>> Show Current State
* terraform state list >>>>>> List All Resources.
* terraform destroy >>>>>>> Destroy Infrastructure
* terraform fmt >>>>>>>> Format Code
* terraform output >>>>>>> Output Values
  



