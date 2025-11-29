Day 2: Temporary User Setup with Expiry 

As part of the temporary assignment to the Nautilus project, a developer named kareem requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed. Here's what you need to do: Create a user named kareem on App Server 1 in Stratos Datacenter. Set the expiry date to 2023-12-07, ensuring the user is created in lowercase as per standard protocol.

---
Explanation-
To create a temporary user account kareem on App Server 1 with an expiry date of 2023-12-07, you can run the following command on the target server:

sudo useradd -e 2023-12-07 kareem

To verify the expiry date was applied correctly:

sudo chage -l kareem 

This will show the account expiration details.

---
