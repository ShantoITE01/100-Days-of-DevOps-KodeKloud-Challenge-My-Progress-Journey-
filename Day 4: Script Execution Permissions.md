In a bid to automate backup processes, the xFusionCorp Industries sysadmin team has developed a new bash script named xfusioncorp.sh. While the script has been distributed to all necessary servers, it lacks executable permissions on App Server 2 within the Stratos Datacenter.

Your task is to grant executable permissions to the /tmp/xfusioncorp.sh script on App Server 2. Additionally, ensure that all users have the capability to execute it. 

Answer:
To make the script executable by all users on App Server 2, you just need to update its permissions.

Here’s exactly what to run on stapp01:

ssh steve@stapp02

# Password: Am3ric@ 

Then 

cd /tmp

Because we go to the tmp file, then run 
---
sudo chmod a+rx /tmp/xfusioncorp.sh
---

Explanation:

•	chmod a+rx → gives read and execute permission to all users (owner, group, others)

•	The script will now be runnable by anyone on the server.

a+rx is shorthand in chmod that means:

a → all users

•	u = user (owner)

•	g = group

•	o = others

•	a = all of the above

rx → add read and execute permission
________________________________________

So chmod a+rx file means:

Give everyone (owner, group, others) permission to read and execute this file.

Because:

•	Without read (r) permission, users cannot read the script content, and many shells require read permission to execute a script from a file.

