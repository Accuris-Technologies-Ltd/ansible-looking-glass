# Ansible-Looking-Glass
## Overview
This ansible role and playbook was created as an automated method to set-up and configure the looking glass application made publicly available at https://github.com/telephone/LookingGlass. This playbook automatically creates the configuration, test and database files required for successful deployment alongside SSL configuration provided that the required ansible variables (see below) are configured in your ansible inventory, and also includes the fix needed to be compatible with PHP version 7.4.

***NOTE: THIS HAS BEEN WRITTEN TO ONLY WORK WITH DEBIAN 10/11 AND UBUNTU 20.04/22.04. A VERSION FOR RHEL-BASED SYSTEMS WILL COME AT A LATER DATE.***


## Inventory Variables
* looking_glass_ipv4 __(Required)__ - The IPv4 address to list on the web page.
* looking_glass_ipv6 (Optional) - The IPv6 address to list on the web page.
* looking_glass_location __(Required)__ - The location where the looking glass is hosted.
* site_name __(Required)__ - The name of the company or network.
* letsencrypt_email __(Required)__ - Email used by Letsencrypt to send you administrative and renewal notices
* test_ratelimit (Optional) - The maximum number of tests allowed per hour per source IP. By default this is disabled however it is recommended to set a reasonable limit to prevent abuse.
