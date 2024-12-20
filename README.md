# SET UP A HYBRID-STORAGE-WITH-AWS-S3-FILE-GATEWAY USING TERRAFORM

USING TERRAFORM TO AUTOMATE THE CREATION OF NFS STORAGE FILE GATEWAY ON AWS FOR AN HYBRID USE WITH ON PREMISES ENVIRONMENT.

This repository contains how to use terraform to setup an AWS storage file gateway for an hybrid cloud solution.

### Important Section

The following are important to have been configured in an on-premises environment.

- Vmware workstation: A Desktop Hypervisor or a VMware vSphere client.
- An OVF template of an AWS S3 type which can be downloaded from the AWS storage gateway console.
- Connect the Vmware workstation to the OVF template and run all the necessary setup and configuration.
- Get the activation key ready.

_**Also, this set up assumes that the gateway will be hosted on a VMware ESXi**_ - as per the AWS supported hosted platform option

### Terraform Code Section

`Provider.tf`: This file will configure the cloud provider as AWS

`S3.tf`: This file will create the S3 bucket for the file gateway.

`Role.tf`: This will create a IAM role with the required permission for the storage gateway access.

`Variable.tf`: This file stores the activation key for the storage gateway.

`Gateway.tf`: This file will setup the storage gateway and the local cache storage for the disks attached to the gateway.

`Fileshare.tf`: Configures an NFS file share for the storage gateway

### Steps to run the code

- Install terraform on machine.
- Make sure the _**Important Section**_ is met.
- Clone the repository and `cd`into the repo directory.
- Enter your activation key in the `Variable.tf` file.
- run `terraform init`
- run `terraform validate`
- run `terraform plan` then run `terraform apply`

### Note

After all command has been successfully...then visit the AWS storage gateway console and under the file share option, copy the mount option for your PC to be used locally via the command line.
