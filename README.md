# devops-vagrant-pipeline
Example pipeline using Vagrant to provision a VM and Ansible to configure Nignx as web server, Consul as Service Discovery, Consul-Template to update Nginx configuration accordingly with registered containers sent by Registrator. All running over Docker

## Requirements
- Vangrant >= 2.2.5
- Libvirt >= 5.1.0

## Goals
- To provide an API Gateway in a single server with basic capabilities
- To dinamically provide Nginx HTTP ingress mechanisms for applications running over Docker with Consul as Service Discovery
- You can recreate the containers and the new instances with different ports will be updated automatically to the Nginx configuration
- For this demo there will be a Redis and an Apache instance running on Docker and available through Nginx

## Running
```
$ vagrant up --provider=libvirt
$ vagrant ssh centos (to connect to the VM provisioned)
$ docker ps (check the container ports)
$ curl http://localhost/httpd
$ curl http://localhost/redis
$ docker restart redis httpd
$ docker ps (check the container ports)
```
