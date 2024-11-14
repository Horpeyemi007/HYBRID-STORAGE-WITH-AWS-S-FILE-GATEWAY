# HYBRID-STORAGE-WITH-AWS-S3-FILE-GATEWAY
USING TERRAFORM TO AUTOMATE THE CREATION OF NFS STORAGE FILE GATEWAY ON AWS FOR AN HYBRID USE WITH  ON PREMISES ENVIRONMENT.

This repository contains how to use terraform to setup an AWS storage file gateway for an hybrid cloud solution.

The following are important to have been configured in an on-premises environment.

* Vmware workstation: A Desktop Hypervisor or a VMware vSphere client.
* An OVF template of an AWS S3 type which can be downloaded from the AWS storage gateway console.
* Connect the Vmware workstation to the OVF template and run all the necessary setup and configuration.
* Get the activation key ready.

Also, this set up assumes that the gateway will be hosted on a VMware ESXi

### Terraform Code Section
