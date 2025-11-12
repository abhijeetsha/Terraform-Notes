# Terraform In One Short-Understanding
## Core Concepts
 * Definations and history of terraform
 * Current Trends & News in terrraform Deployments
 * Insfrastructure as a code (Iac)- Why It Matters.
 * Setup on EC-2 and local machine

## Terraform HCL (Hashicorp Configuration Lauguage) In Depth.
### Basic Syntax:
  * Blocks, Arguments And Attributes.
  * Example:-
  * 
### Types Of Blocks:
 * Providers (aws, azure, Gcp) ---> this is used for access of cloud-platform
   * File Syntax: provider.tf 
 * Resources
 * Variable ---> It is used for verify the value and changes value in main file with the help of variable file.
   * File Syntex: variable.tf
 * Output ---> It is used for its show value on your terminal with the help of output file
   * File Syntax: outputs.tf
 * Modules --->
### Expressions And Functions
 * string Interpolations
 * Loops (for_each, count)
 * Conditionals Expressions

## Terraform Workflow & Executoins
 * Write-Plan-Apply-Workflow
  * terraform init ---> For initializing terraform directory
  * terraform plan ---> Ready For the Execution
  * terraform apply ---> Executed
  * terraform destroy ---> For deleting or destroy.

 ## Terraform CLI And Commands
 ### Core Commands:-
   * terraform init
   * terraform plan
   * terraform apply
   * terraform destroy
   * terraform refresh
   * terraform validate
   * terraform fmt
### Advance Command:-
   * taint
   * import
   * graph
   * state manipulation
* Debugging Terraform Issues
