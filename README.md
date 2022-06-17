# gitlab-azure-challenge

This challenge's objective is to automate the [installation of gitlab on Microsoft Azure](https://docs.gitlab.com/ee/install/azure/#deploy-and-configure-gitlab) (ACloudGuru Azure Sandbox) using Terraform and Ansible.

## Disclaimer

All of the codes and some of the instructions belong to, and copied from another learner - [Brandon](https://github.com/vysky).
The steps below were generated based on my own experience and attempts in running his codes.

You will need to adjust some of the steps if you are not using the same resources as mine.
Resources I used at the time of testing:
- Windows 11 OS
- WSL Ubuntu 20.04
- Visual Studio (VS) Code

Now that it's clear, let's get started.
## Getting Started
### Pre-requisites

Ensure that you have ALL of the following installed and ready on your machine:

1.  Python
2.  [az cli](https://docs.microsoft.com/cli/azure/install-azure-cli)
2.  [Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli)
3.  [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html)
4.  Username and password provided by ACloudGuru (ACG) Azure Sandbox (or your own Azure account)

## Step 1: Cloning The Repo

First, you'll need to clone the correct repo to your desired directory on your machine.
    
1. Open your terminal of choice.
2. Clone Brandon's repo by running the following code:
`git clone https://github.com/vysky/challenge-gitlab.git`
3. Change your directory:
`cd challenge-gitlab/`

## Step 2: Preparing and Running the Terraform File

---

Here, I'm assuming that (1) you have the knowledge on navigating around Azure portal, and (2) you have already prepped and logged into the Azure portal via ACG Azure Sandbox/your own Azure account on your preferred browser.

---

### Preparing the `main.tf` file
1. Go to you Azure portal and copy the generated resource group name to your clipboard.
2. Open the challenge