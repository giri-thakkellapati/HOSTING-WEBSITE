**STEPS FOR HOSTING A WEBSITE**

 * Login into your AWS Account and open EC2-Dashboard
 * Type name of your desirable instance
 * Select instance type (LINUX SERVER)
 * Create new key pair-This key pair will allow you to access using SSH into the machine you just created
 * Configure network setting
 * Configure storage
 * Access your instance by selecting instance then click on connect button.
 * Select SSH client - open terminal and use the below command to access the server.
    -ssh -i “pem file path” ubuntu@instancePublicIP
 * Now you can install nginx
  `  -sudo apt update
    -Sudo apt install nginx
 * To start the service and make sure it remains enable 
    -sudo systemctl start nginx
    -sudo systemctl enable nginx
 * Navigate to NGINX's html directory: cd /var/www/html
   Add files of website to the directory
   Test NGINX config: sudo nginx -t.
 * Restart NGINX: sudo service nginx restart.

 * Access your app using your server's IP
 
**CONNECTING DOMAIN**
 * Access your Namecheap account.

 * Go to advanced DNS settings for your domain.

 * Add Host records
 

**ADDING SSL CERTIFICATE**
 *Install Certbot:
  -sudo snap install --classic certbot
   sudo ln -s /snap/bin/certbot /usr/bin/certbot
   
**CONFORMING NGINXS CONFIGURATION**

 *sudo nano /etc/nginx/sites-available/example.com
 *Update the server name
    ` ...
         server_name example.com www.example.com;
         ...`
 * verify the syntax
   -sudo nginx -t
   -sudo systemctl reload nginx
   
**OBTAINING SSL CERTIFICATE**
 
   *sudo certbot --nginx -d example.com -d www.example.com


























