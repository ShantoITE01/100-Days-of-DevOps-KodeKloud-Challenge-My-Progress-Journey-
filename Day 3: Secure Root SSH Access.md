Day 3: Secure Root SSH Access

Following security audits, the xFusionCorp Industries security team has rolled out new protocols, including the restriction of direct root SSH login.


Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.

Below is the exact step-by-step solution in Bangla + commands to complete the task safely.

________________________________________

✅ Goal

Disable direct SSH root login on all App Servers:

•	stapp01

•	stapp02

•	stapp03

You will do this by editing /etc/ssh/sshd_config.
________________________________________

For Each App Server (stapp01, stapp02, stapp03):

1. SSH into the App Server

stapp01

ssh tony@stapp01

Password: Ir0nM@n


stapp02

ssh steve@stapp02

Password: Am3ric@

stapp03

ssh banner@stapp03

Password: BigGr33n

________________________________________

2. Edit SSH configuration file

Run this on each app server:

sudo vi /etc/ssh/sshd_config

Find the line:

#PermitRootLogin yes

Replace with:

PermitRootLogin no

If the line doesn’t exist, just add it at the bottom.

________________________________________

3. Restart SSH service
   
Run:

sudo systemctl restart sshd
________________________________________

✔️ Verify

Run:

sudo grep PermitRootLogin /etc/ssh/sshd_config

Should show:

PermitRootLogin no
________________________________________

🎯 That’s it!

Root SSH login is now disabled on all three App Servers.
