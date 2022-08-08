# MEDIAWIKI PROBLEM STATEMENT

All the Code used and written in this repo are written by me and using IAC opensoruce tools like Terraform and Ansible

# Problem Statement
The problem statement was to build a complete End to End deployment of [MEDIAWIKI](https://www.mediawiki.org/wiki/MediaWiki) app with Infrastructure Up and Running and Software Configuration Integrated with it on the fly.

>  ### Terraform or any IaC tool with any Configuration Management tool integrated.

---

# Approach
 Provison Infra using Terraform and Configure that infra using Ansible as per the above stated problem statement.

### IAC Tool Used

* Terraform
* Ansible

# Installation

### Install Terraform

To install Terraform, find the [appropriate package](https://www.terraform.io/downloads.html) for your system and download it as a zip archive.

After downloading Terraform, unzip the package. Terraform runs as a single binary named `terraform`. Any other files in the package can be safely removed and Terraform will still function.

Finally, make sure that the `terraform` binary is available on your `PATH`. This process will differ depending on your operating system.

Print a colon-separated list of locations in your `PATH`.
```
    $ echo $PATH
```

Move the Terraform binary to one of the listed locations. This command assumes that the binary is currently in your downloads folder and that your `PATH` includes `/usr/local/bin`, but you can customize it if your locations are different.

```
$ mv ~/Downloads/terraform /usr/local/bin/
```

### Install Ansible

To install Ansible, find the [appropriate flavour](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) for your system

```
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo apt-add-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible
```


#### Directory Structure of Assignment

After Cloning the repo, directory will look something like this :-

```
├───Ansible
│   ├───inventory
│   │   └───group_vars
│   └───playbooks
├───Ansible_roles
│   ├───configuration
│   │   └───tasks
│   ├───MediaWiki
│   │   └───tasks
│   ├───mysql_db
│   │   └───tasks
│   ├───os_packages
│   │   └───tasks
│   ├───service
│   │   └───tasks
│   └───Xampp
│       └───tasks
├───Terraform_files
│   └───tf_files
└───TF_modules
    ├───alb
    ├───ebs
    ├───ec2
    ├───keys
    ├───sg
    └───vpc
```
## Git clone


1. Clone the following Repo

```
git clone https://github.com/upadhyaay/MW_Assessment.git
```

2. Edit the `provider.tf`

- change  the following line and add `{user-name}` with your username
- change `{profile}` with your aws profile with all the access to allow run this terraform code

```
provider "aws" {
  region = "us-east-1"
  shared_credentials_file = "/Users/{user-name}/.aws/credentials"    ## {user-name} : Replace it with your username and path with your to allow access to aws credentials files
  profile                 = "{profile}"                        ## {profile} : Enter the profile that you want to use. By Default the profile is : default
}
```
4. Run the following command to run the `terraform` code

```
terraform init
terraform plan
terraform apply
```

5. Run the Ansible Playbooks for further configuration on top of the Infrastructure provisioned.
```
ansible-playbook <playbookname.yml>