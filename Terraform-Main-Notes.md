# Terraform Main Notes On Topics.
## 🌍 1. Terraform Basic Concepts
### Ans: Terraform is an Infrastructure as Code (IaC) tool created by HashiCorp.
* It allows you to define, provision, and manage infrastructure across multiple cloud providers (AWS, Azure, GCP, etc.) using declarative configuration files.
## Key Components:
   * Provider: Plugin that interacts with a specific platform (e.g., AWS, Azure, GCP).
   * Resource: The basic building block (e.g., aws_instance, aws_s3_bucket).
   * Data Source: Reads data from existing infrastructure.
   * Input Variables: External values provided to configurations.
   * Output Values: Displayed or used by other configurations.
   * Module: Reusable group of Terraform resources.
   * State File: Tracks the current state of your infrastructure.

## 📜 2. Terraform HCL (HashiCorp Configuration Language)
### Ans: HCL is Terraform’s domain-specific language for writing configuration files.
* Files typically end with .tf extension.

### Example:
* provider "aws" {
  * region = "us-east-1"
* }

* resource "aws_instance" "web" {
  * ami           = "ami-0c55b159cbfafe1f0"
  * instance_type = "t2.micro"
  * tags = {
    * Name = "MyServer"
  * }
* }
### ✅ Readable, declarative, and supports interpolation using ${} syntax or modern direct expressions.

## ⚙️ 3. Terraform Workflow & Execution
### Terraform workflow follows five key steps:
| Step           | Command             | Description                                      |
| -------------- | ------------------- | ------------------------------------------------ |
| **1. Write**   | `.tf` files         | Define resources                                 |
| **2. Init**    | `terraform init`    | Initialize project and download provider plugins |
| **3. Plan**    | `terraform plan`    | Preview infrastructure changes                   |
| **4. Apply**   | `terraform apply`   | Create or modify resources                       |
| **5. Destroy** | `terraform destroy` | Delete resources                                 |

## 💻 4. Terraform CLI & Commands
| Command               | Purpose                                        |
| --------------------- | ---------------------------------------------- |
| `terraform init`      | Initializes Terraform working directory        |
| `terraform plan`      | Shows what actions Terraform will perform      |
| `terraform apply`     | Executes the plan and provisions resources     |
| `terraform destroy`   | Removes all managed infrastructure             |
| `terraform validate`  | Checks configuration syntax                    |
| `terraform fmt`       | Formats code style                             |
| `terraform show`      | Displays state or plan                         |
| `terraform output`    | Displays output variables                      |
| `terraform state`     | Manages the Terraform state file               |
| `terraform workspace` | Manages multiple environments (dev/stage/prod) |

## 🔢 5. Terraform Variables & Expressions
### Variables make configurations flexible and reusable.

## Types:
* Input Variables: Defined using variable block.
* Local Variables: Defined using locals block.
* Output Values: Defined using output block.

## Example:
* variable "instance_type" {
  * type    = string
  * default = "t2.micro"
* }

* locals {
  * project = "myapp"
* }

* output "instance_id" {
  * value = aws_instance.web.id
* }

## Expressions allow:
* String interpolation → "Hello ${var.name}"
* Conditionals → var.env == "prod" ? "t3.medium" : "t2.micro"
* Functions → length(var.list), upper(var.name)

## 🗂️ 6. Terraform State Management & Backends
### Terraform uses a state file (terraform.tfstate) to record what resources exist in the real world.
## Purposes:
   * Maps resources in config to real infrastructure.
   * Detects changes between desired and actual states.
## State Backends:
* Local backend (default) → stores terraform.tfstate locally.
* Remote backend → stores in cloud storage for collaboration, e.g.:
    * AWS S3 (with DynamoDB locking)
    * Terraform Cloud
    * Azure Blob Storage
    * Google Cloud Storage
