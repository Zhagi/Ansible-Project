# Ansible Web Server Configuration Project

## Overview
This repository is part of an Ansible learning exercise designed to automate the process of configuring a web server on a remote Ubuntu machine. The primary focus is to apply basic Ansible concepts to perform common server setup tasks.

![Ansible Setup & Workflow Architecture](images/Ansible_Setup_Workflow_Architecture.png)

## Project Description
The included Ansible playbook (`web_server_setup.yml`) performs the following actions:
- **Update package manager cache**: Ensures the package list is up to date before installing any new packages.
- **Install Apache**: Installs the Apache web server package.
- **Start Apache service**: Ensures the Apache service is enabled to start on boot and is running.
- **Deploy custom HTML page**: Places a simple `index.html` file in the web server's document root (`/var/www/html`) that displays "Hello, Ansible!".

## Infrastructure Setup
The infrastructure for this project is set up on AWS. Below is the summary of the EC2 instance used for the web server.

![EC2 Instance Summary](images/EC2_instance_summary.png)

The AMI used for the EC2 instance is Ubuntu, as shown below:

![Ubuntu AMI Used](images/Ubuntu_AMI_used.png)

## Execution Results
After running the Ansible playbook, the following tasks were completed successfully, as shown in the terminal output:

![Terminal Output Showing Completed Tasks](images/Terminal_output_showing_completed_tasks.png)

The resulting web server is accessible through the browser:

![Web Server Running](images/Web_server_running.png)

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

## License
This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.

## Acknowledgements
- Thanks to the Ansible community for providing excellent documentation and resources.
- This project was created as part of a learning exercise for automating server setups.




![Diagram]
