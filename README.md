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

This project involves deploying a Node.js application on Google Kubernetes Engine (GKE) using Docker images. The application consists of a frontend service and a backend service, both of which are deployed using Kubernetes manifests. The backend service includes a database that is deployed using StatefulSets for persistent storage.

## Live Application

You can access the live application at the following URL:

- **Frontend Service:** [http://34.27.131.89:3000](http://34.27.131.89:3000)

## Kubernetes Deployment

### Kubernetes Objects Used

1. **Deployments**: Used for deploying and managing the frontend and backend services.
2. **Services**: Exposes the frontend and backend pods. The frontend service uses a LoadBalancer to provide an external IP address.
3. **StatefulSets**: Used for deploying the MongoDB database to ensure stable network identities and persistent storage.

### Method to Expose Pods to Internet Traffic

- The **frontend-service** is exposed using a `LoadBalancer` type service, which provides an external IP address to access the application from outside the Kubernetes cluster.

### Persistent Storage

- The MongoDB database is deployed using StatefulSets to ensure data persistence and stability.


