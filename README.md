Building and configuring a firewall is crucial for protecting networks from unauthorized access and potential threats. This is guide for you through to set up and configuring a firewall on an Ubuntu system using UFW (Uncomplicated Firewall).<br>
<br>
**Prerequisites:**<br>
1.Basic knowledge of Linux commands<br>
2.An Ubuntu system (physical or virtual machine)<br>
3.Root or sudo access<br>
<br>
**Step-by-Step Guide**<br>
Step 1: Update Your System<br>
Ensure your system is up to date.<br>
```sudo apt update```<br>
```sudo apt upgrade -y```<br>
<br>
Step 2: Install UFW<br>
UFW is included in most Ubuntu installations by default, but you can install it if it's not present.<br>
```sudo apt install ufw```<br>
<br>
Step 3: Enable UFW<br>
By default, UFW is disabled after installation. Enable it with the following command:<br>
```sudo ufw enable```<br>
You will be prompted to confirm the action. Type `y` and press "Enter".<br>
<br>
Step 4: Allow SSH Connections<br>
To prevent locking yourself out of the system, allow SSH connections:<br>
```sudo ufw allow ssh```<br>
<br>
Alternatively, you can specify the port number (default is 22):<br>
```sudo ufw allow 22/tcp```<br>
<br>
Step 5: Allow Specific Services and Ports<br>
You can configure UFW to allow specific services and ports based on your needs. Here are some
common examples:<br>
1. Allow HTTP and HTTPS traffic:<br>
```sudo ufw allow http```<br>
```sudo ufw allow https```<br>
Or by specifying the ports:<br>
```sudo ufw allow 80/tcp```<br>
```sudo ufw allow 443/tcp```<br>
2. Allow other specific ports:<br>
For example, to allow traffic on port 8080:<br>
```sudo ufw allow 8880/tcp```<br>
3. Allow a range of ports:<br>
```sudo ufw allow 1000:2000/tcp```<br>
4. Allow specific IP addresses:<br>
To allow connections from a specific IP address (e.g., 192.168.1.100):<br>
```sudo ufw allow from 192.168.1.100```<br>
5. Allow specific subnets:<br>
```sudo ufw allow from 192.168.1.0/24```<br>
<br>
Step 6: Deny Specific Services and Ports<br>
by default, UFW blocks all incoming connections except for the ones explicitly allowed. You can lso specify to deny certain connections explicitly.<br>
1. Deny a specific port:<br>
```sudo ufw deny 23/tcp```<br>
2. Deny a specific IP address:<br>
```sudo ufw deny from 283.0.113.0```<br>
<br>
Step 7: View UFW Status and Rules<br>
check the status of UFW and view the current rules:<br>
```sudo ufw status verbose```<br>
<br>
Step 8: Delete UFW Rules<br>
If you need to remove a rule, you can delete it using its rule number or the exact rule specification.<br>
1. Using rule number:<br>
First, list the rules with numbers:<br>
```sudo ufw status numbered```<br>
Then delete a rule by specifying its number:<br>
```sudo ufw delete 2```
