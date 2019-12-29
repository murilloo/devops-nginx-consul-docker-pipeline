# devops-vagrant-pipeline
Example pipeline using Vagrant to provision a VM and Ansible to configure Nignx as web server, Consul as Service Discovery, Consul-Template to update Nginx configuration accordingly with events fired by Registrator running over Docker

## Requirements
- Vangrant >= 2.2.5
- Libvirt >= 5.1.0

## Goals
- To have an API Gateway running over Nginx in a single server with Consul and Docker
- To dinamically provides HTTP entry points to backend services to Nginx running over Docker and using Consul as Service Discovery
