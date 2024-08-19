# 1. Install the required software
# Install Docker
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

# Install Vagrant
wget https://releases.hashicorp.com/vagrant/2.3.4/vagrant_2.3.4_x86_64.deb
sudo apt install ./vagrant_2.3.4_x86_64.deb

# Install VirtualBox
sudo apt-get install virtualbox

# Install Ansible
sudo apt-get update

sudo apt-get install software-properties-common

sudo apt-add-repository --yes --update ppa:ansible/ansible

'sudo apt-get install ansible'

# 2. Clone the repository and navigate to the client and backend folders
-git clone https://github.com/Scolasticah4/yolo

'cd yolo/client'

'npm install'

'npm start'

'cd ../backend'

'npm install'

'npm start'

# 3. Set up a Vagrant environment and run the Ansible playbook
'cd ..'

'vagrant init'
# Edit the Vagrantfile to choose the base box, for example:
# config.vm.box = "ubuntu/focal64"
'vagrant up'

'ansible-playbook playbook.yaml'

# Access the application
-Open your web browser and go to http://localhost:3000/

# Stop the application
-Press Ctrl+C in the terminal

# Terminate the application
'vagrant destroy'

# My Kubernetes Project

## Overview
This project involves deploying a Node.js application on Google Kubernetes Engine (GKE) using Docker images.

## Setup Instructions
1. Clone the repository.
2. Install dependencies.
3. Configure environment variables.

## Deployment Instructions
1. Apply Kubernetes manifests: `kubectl apply -f manifests/`
2. Verify the deployment: `kubectl get pods,svc`

## Usage
Access the frontend at [http://34.27.131.89:3000](http://34.27.131.89:3000) and interact with the cart functionality.


