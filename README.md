# Ansible Web Server Configuration Project

## Overview
This repository is part of an Ansible learning exercise designed to automate the process of configuring a web server on a remote Ubuntu machine. The primary focus is to apply basic Ansible concepts to perform common server setup tasks.

![Ansible Setup & Workflow Architecture](https://github.com/Zhagi/Ansible-Project/blob/main/Images/Ansible%20Setup%20&%20Workflow%20Architecture.png?raw=true)

## Project Description
The included Ansible playbook (`web_server_setup.yml`) performs the following actions:
- **Update package manager cache**: Ensures the package list is up to date before installing any new packages.
- **Install Apache**: Installs the Apache web server package (apache2).
- **Start Apache service**: Ensures the Apache service is enabled to start on boot and is running.
- **Deploy custom HTML page**: Places a simple `index.html` file in the web server's document root (`/var/www/html`) that displays "Hello, Ansible!".

## Infrastructure Setup
The infrastructure for this project is set up on AWS. Below is the summary of the EC2 instance used for the web server.

![EC2 Instance Summary](https://github.com/Zhagi/Ansible-Project/blob/main/Images/EC2%20instance%20summary.png?raw=true)

The AMI used for the EC2 instance is Ubuntu, as shown below:

![Ubuntu AMI Used](https://github.com/Zhagi/Ansible-Project/blob/main/Images/Ubuntu%20AMI%20used.png?raw=true)

## Execution Results
After running the Ansible playbook, the following tasks were completed successfully, as shown in the terminal output:

![Terminal Output Showing Completed Tasks](https://github.com/Zhagi/Ansible-Project/blob/main/Images/Terminal%20output%20showing%20completed%20tasks.png?raw=true)

The resulting web server is accessible through the browser:

![Web Server Running](https://github.com/Zhagi/Ansible-Project/blob/main/Images/Web%20server%20running.png?raw=true)

## Prerequisites
- An Ubuntu server with SSH access.
- Ansible installed on your local machine.
- The server's IP address or hostname is listed in the Ansible inventory file (`hosts`).

## Usage
To use this playbook:
1. Clone the repository to your local machine.
git clone https://github.com/Zhagi/Ansible-Project.git
2. Navigate to the cloned directory.
cd ansible-project
3. Run the playbook using the following command.
ansible-playbook -i hosts web_server_setup.yml

## Security
Please ensure that you have configured your server's security settings, including firewalls and security groups, to allow traffic on the required ports (SSH and HTTP by default).

## Contributing
Contributions to this project are welcome! Please fork the repository and submit a pull request with your improvements.

## Acknowledgements
- This project is part of a comprehensive exercise aimed at mastering the automation of server configurations. You can explore this project along with others at [moabukar/tech-vault](https://github.com/moabukar/tech-vault).


