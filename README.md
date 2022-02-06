Please see https://unofficialaciguide.com

Used for POC:  Cisco Cloud ACI Generic External Connectivity.  https://unofficialaciguide.com/2022/01/20/cisco-cloud-aci-generic-external-connectivity/

This spins up a VPC, IGW & EC2.  ssh keys are imported from local machine you are using

# Usage:
```
git clone https://github.com/soumukhe/Terraform-aws-physical-dummy.git
cd Terraform-aws-physical-dummy
modify the overfide.tf file and put in your aws credentials for the account where this will be spun up (could be the same ACI tenant account)
modify terraform.tfvars file as needed
terraform init
terraform validate
terraform apply
```
If you needed to change names,IPs hardcoded in main.tf, please vi and change appropriately.
as an example,  to change VPC names and everything associated with name from aws-phy-dummy to aws-brfiwnfield you can simply use:
```
sed -i 's/phy-dummy/brownfield/g' main.tf
```
Public IP will spit out on screen after terraform apply.  You could also do terraform refresh followed by terraform output to view it later.
