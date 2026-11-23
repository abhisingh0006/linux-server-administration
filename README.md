
# Linux Server Administration & Web Application Deployment

## Project Overview

This project demonstrates the deployment of a basic Node.js web application on an AWS EC2 Ubuntu server.

The application is managed using PM2 and exposed to the internet through Nginx as a reverse proxy.

The main objective was to gain practical experience with Linux server administration, AWS EC2, application deployment, process management, and web server configuration.

## Architecture

User Browser
    |
    v
AWS EC2 - Ubuntu 24.04
    |
    v
Nginx (Port 80)
    |
    v
Node.js / Express Application (Port 3000)
    |
    v
PM2 Process Manager

## Technologies Used

- AWS EC2
- Ubuntu Server 24.04 LTS
- Linux
- Node.js
- Express.js
- Nginx
- PM2
- Git

## Project Implementation

### 1. AWS EC2 Setup
- Launched an Ubuntu 24.04 EC2 instance.
- Configured the instance security group.
- Connected to the server using SSH from Windows PowerShell.

### 2. Linux User Management
- Created a separate Linux user named `deployer`.
- Added the user to the required groups.
- Practised Linux ownership and permission management.

### 3. Application Setup
- Installed Node.js and npm.
- Created a Node.js application using Express.js.
- Installed the required application dependencies.

### 4. Process Management with PM2
- Installed PM2 globally.
- Started the Node.js application using PM2.
- Configured PM2 to start the application after a server reboot.
- Saved the PM2 process list.

### 5. Nginx Configuration
- Installed and enabled Nginx.
- Configured Nginx as a reverse proxy.
- Forwarded incoming HTTP requests on port 80 to the Node.js application on port 3000.
- Tested the Nginx configuration and verified the application response.

### 6. Application Verification

Expected application response:

`Complaint Portal Server is Running!`

## Linux Commands Practised

| Command | Purpose |
|---|---|
| `pwd` | Display current directory |
| `ls -la` | List files and permissions |
| `cd` | Change directory |
| `mkdir` | Create a directory |
| `touch` | Create a file |
| `cat` | Display file contents |
| `chmod` | Change file permissions |
| `chown` | Change file ownership |
| `whoami` | Display current user |
| `id` | Display user and group details |
| `df -h` | Check disk usage |
| `free -h` | Check memory usage |
| `sudo` | Execute commands with elevated privileges |
| `systemctl` | Manage system services |
| `curl` | Test HTTP endpoints |

## Application Management Commands

```bash
pm2 start app.js --name complaint-portal
pm2 status
pm2 logs complaint-portal
pm2 restart complaint-portal
pm2 save
```

## Nginx Management Commands

```bash
sudo systemctl status nginx
sudo systemctl start nginx
sudo systemctl enable nginx
sudo nginx -t
sudo systemctl reload nginx
```

## Learning Outcomes

- Hands-on experience with AWS EC2.
- Linux server access and administration using SSH.
- Linux users, groups, ownership and permissions.
- Node.js application deployment.
- Application process management using PM2.
- Nginx reverse proxy configuration.
- Basic server troubleshooting and connectivity testing.

## Project Scope

This project covers basic server administration and deployment only.

Database integration, frontend development, authentication, and complaint management functionality are not included. These may be explored in a separate future project.

## Author

Abhishek Singh

B.Tech - Information Technology
