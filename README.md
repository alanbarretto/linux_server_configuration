# Linux Server Configuration

The Linux Server Configuration Project is about configuring a Linux server and preparing it to host a web application. The server is secured  from a number of attack vectors. A database server is installed and configured , and an existing web application is deployed onto it.

## Components for grader Access

1. IP Address:  54.245.174.21
2. SSH Port: 2200
3. Complete URL to hosted web application: http://ec2-54-245-174-21.us-west-2.compute.amazonaws.com

## Summary of Software Installed

1. Python 3
2. Flask
3. Sqlalchemy.orm
4. Oauth2client
5. Postgresql
6. Psycopg2
7. Python 3 mod_wsgi package
8. Git
9. NTP
10. Apache2
11. Finger

## Configurations Made

1. Created user named 'grader' and gave sudo access by adding grader to sudoers file.
2. Enforced Key-based Authentication.
3. Disabled remote user login.
4. Disabled Password based logins by modifying the sshd_config file.
5. Changed SSH port from 22 to 2200. 
6. Disabled SSH Port 22, then Allowed Port 123.
7. Configured UFW to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
8. Disabled remote connections for PostgreSQL.
9. Created New Role 'catalog' in postgres with limited permissions, and created database 'car_catalog'.
10. Configured NTP local timezone to UTC.

## Third Party Resources Used

1. Google OAuth2 Third Party Authentication - a client_secrets.json file was downloaded from the Google console, and the complete URL was included in the Authorized JS origins and redirects.

## Web App Deployed

Udacity Item Catalog Project - The App “Joe’s Used Car Lot” allows users who are logged in to post their vehicles for sale. It can be posted in one of the numerous categories, or a user can create an exclusive space called a “garage” where all their vehicles can be posted in one place. However, vehicles posted in garages will also show up in the appropriate categories. So, if a user creates a garage and posts an SUV there, potential buyers will find that vehicle in that garage as well as in the SUV category.

## Known Bugs

Facebook Third Party Authentication is not available at this time due to changes being made on their security protocols. News of this issue can be found through this link:  https://newsroom.fb.com/news/2018/03/cracking-down-on-platform-abuse/

