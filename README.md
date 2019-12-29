# devops-vagrant-pipeline
Example pipeline using Vagrant for provisioning a VM and Ansible to configure Nignx as web server, Consul as Service Discovery, consul-template to update Nginx configuration accordingly with events fired by Registrator running over Docker

## Requirements
- Vangrant >= 2.2.5
- Libvirt >= 5.1.0

## Goals
- To have an API Gateway running over Nginx in a single server
- To dinamically provides HTTP entry points to backend services running over Docker
