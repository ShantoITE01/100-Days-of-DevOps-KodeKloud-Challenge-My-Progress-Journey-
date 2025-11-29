---
Question:

To accommodate the backup agent tool's specifications, the system admin team at xFusionCorp Industries requires the creation of a user with a non-interactive shell. Here's your task:

Create a user named siva with a non-interactive shell on App Server 1.

Note: You can find infrastructure details by clicking the " Details of all Users and Servers " button in the top-right section of the page.

---

Answer:

Explaination
Create a user named siva with a non-interactive shell on App Server 1.

A non-interactive shell means:

•	The user cannot log in

•	The user has no terminal access

•	It is used for service accounts / backup agents/automation users.

Example of a non-interactive shell:

/sbin/nologin

________________________________________

✅ What you did in the screenshot

1️⃣ Logged into App Server 1

ssh tony@stapp01

2️⃣ Created the user with a non-interactive shell

sudo useradd -s /sbin/nologin siva

•	useradd → creates a new user

•	-s /sbin/nologin → assigns a non-interactive shell

(so the user cannot log in)

3️⃣ Checked the user entry

grep siva /etc/passwd

Output shows:

siva:x:1002:1002::/home/siva:/sbin/nologin

This means:

•	Username → siva

•	Home directory → /home/siva

•	Shell → /sbin/nologin ✔️ (correct)

________________________________________

⭐ Conclusion

Your work is 100% correct:

•	User created: ✔️

•	Non-interactive shell assigned: ✔️

•	Verified in /etc/passwd: ✔️



