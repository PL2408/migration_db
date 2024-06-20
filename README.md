# migration_db

# Backup and Deploy MySQL Database

This project demonstrates how to backup a MySQL database from a production server and deploy it to a development server using GitHub Actions.

## Prerequisites

- Two VirtualBox machines: `prod` and `dev`
- MySQL server installed on both machines
- SSH keys set up for both machines
- A GitHub repository for the project

## Steps

### 1. Install MySQL on `dev` Server

```sh
sudo apt update
sudo apt install mysql-server -y
sudo systemctl start mysql
sudo systemctl enable mysql

2. Create a GitHub Repository
Create a new GitHub repository named migration_db and clone it to your local machine.

3. Setup Local Repository and Connect to GitHub
git init
git remote add origin git@github.com:yourusername/migration_db.git

4. Add SSH Keys and Secrets
Add the following secrets in your GitHub repository settings:

SSH_KEY: Private SSH key for accessing your servers
DB_USER: MySQL username
DB_PASSWORD: MySQL password
DB_NAME: MySQL database name
LOGIN_HOST: IP address or hostname of the prod server
LOGIN_USER: SSH username for the prod server
PORT: SSH port (default is 22)

5. Create GitHub Actions Workflow
6. Manually Verify the Database on dev Server
