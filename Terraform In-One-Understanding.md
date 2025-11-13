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

## Terraform Variable & Expressions
### Types Of Variable
  * Input Variables (variable)
  * Output Variable (outputs)
  * Local Variable (Locals)
### Dynamic Configurations
  * Conditional Expressions
  * Dyanamics Block (For_each, Count)

## Terraform State Manageentes & Backends
  * Role Of State In Infrastructure Management
    * terraform state list
    * terraform state show
    * terraform apply
    * terraform import <name> <id>
    * In This you can import existing EC-2 server, S-3 buckets, your keys ETC.
    * It is the used of maintain AWS infras
  * Secuer State Managemenet Best Practices
  * Remote state Backend.
   * AWS S3 For Remote Storage.
     * Create s3-bucket s3.tf 
   * State Locking With DynamoDB.
     * Create DyanamoDb.tf
     * terraform init
     * terraform plan
     * terraform apply

 ## Terraform Provisioner and user data
  * Understanding Provisioner
   * file, local exec, remote-exec.
   * Use Cases For Provisioners
   * Using User data with AWS ec-2

## Terraform Workspaces And Enviroment Managements
 * What are the workspaces.
 * Managing Multiple Enviroments (Dev, Stagging And Prod)
 * Creating And Swtiching Workspaces.

## Terraform Modules - Reusability & Best Practices.
 * What are modules
 * using prebuilt modules from terraform registry
 * Creating Custom Modules
  * Module Structure, Best Practices And Outputs.
 
