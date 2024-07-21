Building and configuring a firewall is crucial for protecting networks from unauthorized access and potential threats. This tutorial will guide you through setting up and configuring a firewall on an Ubuntu system using UFW (Uncomplicated Firewall).
******Prerequisites*****
>Basic knowledge of Linux commands
>An Ubuntu system (physical or virtual machine)
>Root or sudo access
******Step-by-Step Guide*****

Step 1: Update Your System
Ensure your system is up to date.
bash
sudo apt update
sudo apt upgrade -y
Step 2: Install UFW
Copy code
UFW is included in most Ubuntu installations by default, but you can install it if it's not present.
bash
sudo apt install ufw
Step 3: Enable UFW
By default, UFW is disabled after installation. Enable it with the following command:
bash
sudo ufw enable
You will be prompted to confirm the action. Type `y` and press "Enter`.
Step 4: Allow SSH Connections
To prevent locking yourself out of the system, allow SSH connections:
bash
sudo ufw allow ssh
Copy code
Copy code
Copy code
