# Mere Medical Network Project

This project deploys Mere Medical inside an Ubuntu Server virtual machine running on Proxmox.

## Components

- Mere Medical
- WordPress
- MySQL
- OAuth2 Proxy
- OAuth 2.0 / OpenID Connect integration
- Containerlab virtual network
- Custom WordPress integration plugin
- Docker and Docker Compose
- zrok public sharing

## Architecture

- Proxmox hosts the Ubuntu Server virtual machine.
- Docker Compose runs Mere Medical, WordPress, MySQL, and OAuth2 Proxy.
- WordPress acts as an OAuth 2.0 / OpenID Connect identity provider.
- OAuth2 Proxy protects access to Mere Medical.
- Containerlab creates two clients and one medical server.
- The WordPress plugin displays the application status and integration details.

## Local URLs

- WordPress: `http://SERVER_IP:8080`
- Mere Medical direct access: `http://SERVER_IP:4201`
- OAuth-protected Mere Medical: `http://SERVER_IP:4200`

## Security

Environment files, passwords, client secrets, database credentials, and zrok credentials are excluded from Git.
