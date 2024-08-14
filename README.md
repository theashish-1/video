Step 1 : Generate a ssl certificate 
Steps to generate ssl certificate 
open gitbash or command prompt and type mkdir ssl 
next type this command
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ssl/private_key.pem -out ssl/certificate.pem -subj "//C=US//ST=California//L=San Francisco//O=MyOrganization//OU=MyDepartment//CN=<YOUR_LOCAL_IP>"

Steps 2 : update nginx.conf
change <YOUR_LOCAL_IP> with your local ip

Step 3 : update client.js file in resources
update LOCAL_IP_ADDRESS to your local ip address

Step 4 : build docker image using the below command
docker-compose up -d --build
