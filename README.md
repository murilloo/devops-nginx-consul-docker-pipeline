# devops-vagrant-pipeline
Example pipeline using Vagrant to provision a VM and Ansible to configure Nignx as web server, Consul as Service Discovery, Consul-Template to update Nginx configuration accordingly with registered containers sent by Registrator. All running over Docker

## Requirements
- Vangrant >= 2.2.5
- Libvirt >= 5.1.0

## Goals
- To have an API Gateway running over Nginx in a single server with Consul and Docker
- To dinamically provide Nginx HTTP/HTTPS Ingress mechanisms for frontend and backend applications running over Docker and using Consul as Service Discovery
