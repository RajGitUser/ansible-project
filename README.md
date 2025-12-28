# ansible-project

A collection of Ansible automation playbooks, inventory, and configuration files to automate the provisioning and configuration of application services and their dependencies.

This repository helps you deploy microservices (e.g., catalogue, cart, payment, shipping, user), databases, and infrastructure components using Ansible. 
GitHub

# 🧠 About

This repository contains Ansible playbooks, inventory definitions, and configuration templates that automate the deployment and setup of services, databases, and related infrastructure settings.
It can be used to standardize deployments, reduce manual configuration effort, and ensure consistent environments across systems. 
GitHub

> YAML files are Ansible playbooks for provisioning services and dependencies.  
> `.service` files define systemd service units. Repo files configure package repositories.  
> `inventory.ini` lists target hosts/groups for automation. :contentReference[oaicite:4]{index=4}

---

## 🧰 Prerequisites

Before running these playbooks, make sure:

✔ Ansible is installed on your control node (e.g., `apt install ansible` or via `pip`)  
✔ You have SSH access (with keys) to target hosts  
✔ Your inventory (`inventory.ini`) contains correct host entries and groups  
✔ Target systems have Python installed (required by Ansible) :contentReference[oaicite:5]{index=5}

---

## 🚀 Usage

1. Clone the Repository

```bash
git clone https://github.com/RajGitUser/ansible-project.git
cd ansible-project

2. Update Inventory

Edit inventory.ini to reflect your target hosts:

[app_servers]
server1 ansible_host=IP_ADDRESS
server2 ansible_host=IP_ADDRESS

[db_servers]
db1 ansible_host=IP_ADDRESS

3. Run a Playbook
ansible-playbook -i inventory.ini catalogue.yaml


You can replace catalogue.yaml with any other playbook file (e.g., mongodb.yaml, redis.yaml). 
GitHub

📄 Playbooks & Configurations
File	                          Purpose
01-ec2-r53.yaml	                Initial setup (e.g., AWS EC2 + Route53 tasks)
catalogue.yaml	                Deploy and configure the catalogue service
cart.yaml	                      Deploy and configure the cart service
payment.yaml	                  Deploy and configure the payment service
shipping.yaml	                  Deploy and configure the shipping service
user.yaml	                      Deploy and configure the user service
mongodb.yaml	                  Setup MongoDB
redis.yaml	                    Setup Redis
mysql.yaml	                    Setup MySQL
mongo.repo,                     rabbitmq.repo	Repo configs for packages
*.service	                      Systemd service definitions for each microservice
nginx.conf	                    NGINX configuration template


Contributions are welcome! To improve this project:

Fork the repository

Create a new feature branch

Add or update playbooks/configs

Submit a Pull Request

Clear documentation and consistent YAML formatting help maintain quality.
