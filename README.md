
# Ansible-Based Portfolio Website Deployment

## Project Overview

This project demonstrates the automated deployment of a static portfolio website on an AWS EC2 Ubuntu server using Ansible Roles and Nginx.

Ansible automates server configuration, Nginx installation, and deployment of website files.

## Technologies Used

- AWS EC2 – Cloud infrastructure
- Ubuntu Linux – Operating system
- Ansible – Configuration management
- Nginx – Web server
- HTML5 – Website structure
- CSS3 – Website styling
- Git and GitHub – Version control

## Project Structure

```text
ansible-portfolio-deployment/
├── inventory/
│   └── inventory.ini
├── roles/
│   └── portfolio/
│       ├── files/
│       │   ├── index.html
│       │   ├── about.html
│       │   ├── projects.html
│       │   ├── contact.html
│       │   └── style.css
│       └── tasks/
│           └── main.yml
├── screenshots/
├── site.yml
├── README.md
└── .gitignore
```

## Infrastructure

Two AWS EC2 instances are used:

- **Control Node:** Runs Ansible and initiates deployment.
- **Target Node:** Hosts the website using Nginx.

Ansible communicates with the target server through SSH.

## Deployment Process

1. Configure AWS EC2 instances.
2. Install Ansible on the control node.
3. Configure SSH connectivity.
4. Define the target server in the inventory.
5. Create the reusable portfolio role.
6. Install Nginx using Ansible.
7. Copy website files into `/var/www/html/`.
8. Start and enable Nginx.
9. Verify the website using the target EC2 public IP.

## Execute Deployment

From the project root, run:

```bash
ansible-playbook -i inventory/inventory.ini site.yml
```

## Live Website

http://13.62.52.66

## Screenshots

Deployment screenshots are available in the `screenshots/` directory.

## Deployment Result

The Ansible playbook executed successfully with zero failed and unreachable hosts.

The portfolio website was successfully deployed and verified using Nginx on AWS EC2.

---

**Project:** Portfolio Website Deployment Using Ansible Roles  
**Platform:** AWS EC2  
**Web Server:** Nginx
