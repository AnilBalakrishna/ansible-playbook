# Automated Container Deployment

[![Ansible](https://img.shields.io/badge/Ansible-2.9%2B-red)](https://docs.ansible.com/)
[![Docker](https://img.shields.io/badge/Docker-20.10%2B-blue)](https://docs.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## Project Purpose

This project automates the deployment of an Apache web server using Ansible and Docker with custom network configuration. It demonstrates infrastructure as code principles by providing reusable automation scripts for containerized web service deployment.

## Technologies Used

- **Ansible**: Configuration management and automation engine
- **Docker**: Containerization platform
- **Apache HTTP Server (httpd)**: Web server software
- **Docker SDK for Python**: Python library for Docker API interaction
- **Mermaid**: Diagramming and charting tool

## Architecture Overview

The project deploys an Apache container with the following specifications:
- Custom Docker bridge network: `apache_network` (172.168.10.0/30)
- Container IP address: 172.168.10.2
- Port mapping: Host port 8080 → Container port 80
- Restart policy: Always
- Static HTML content serving

## Prerequisites

### System Requirements
- Linux-based operating system (Ubuntu 18.04+ recommended)
- Python 3.6 or higher
- Internet connectivity for downloading Docker images

### Required Software
Before running this automation, ensure the following are installed on your target machine:

1. **Docker Engine**
   ```bash
   # Install Docker (Ubuntu/Debian)
   curl -fsSL https://get.docker.com -o get-docker.sh
   sudo sh get-docker.sh
   sudo usermod -aG docker $USER
   