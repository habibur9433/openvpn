# Deploy VPN server in AWS using OPENVPN AMI from AWS marketplace 

Log in to your AWS Management Console.
Go to the AWS Marketplace and search for "OpenVPN Access Server."
Choose an OpenVPN Access Server AMI that suits your needs and region.

Launch an Instance:
Click "Continue to Subscribe" and then "Continue to Configuration."
Configure your instance settings, such as instance type, subnet, security groups, and key pair.
Review and launch the instance.

Connect to the Instance:
Once the instance is running, use SSH to connect to it using the key pair you selected during launch.
example: ssh -i "your keypair name" root@ec2-(instance's ip).compute-1.amazonaws.com

After connecting to the instance, you'll need to run the initial setup following the Setup Wizar.
The setup wizard will guide you through various configuration options, including the admin username and password, hostname, and licensing.

Access the Admin Web Interface:
After completing the setup, access the Admin Web Interface using your instance's public IP address on port 943 (e.g., https://your_instance_ip:943/admin).

Log In and Configure Clients:
Log in using the admin credentials you set during the setup.
Navigate to "User Permissions" to add users and generate client profiles.
Download the client profiles (e.g., .ovpn files) for your client devices from the Admin Web Interface.
Install OpenVPN Client and Import Profile:

Install the OpenVPN client software on your client devices.
Import the downloaded client profile into your OpenVPN client software.
Connect to the OpenVPN Server:

Use your OpenVPN client software to connect to the server using the imported client profile.
You might be prompted to enter the username and password you created in the Admin Web Interface.

Test the Connection:
Once connected, test the VPN connection by accessing resources within your private network or verifying your IP address.
