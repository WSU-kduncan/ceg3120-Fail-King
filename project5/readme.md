# Project 5

## etc/hosts and ssh

###
In the hosts file we associate the private ip to a human readable name

I have set up the proxy's host file so now I can just connect using the private IP's of the other instances by using server1 and server2.  To achieve this I scp'ed my private key from my personal machine to the proxy machine. 

## haproxy config
   
### 
1. sudo apt install -y haproxy
2. /etc/haproxy/haproxy.cfg was edited
3. I set the mode to tcp as we did for lecture, as well as an option for the log to be a tcp log.  I kept all of the error files that were in the original cfg.  I added the frontend block and renamed it to my www.cskIIsite.com.  I bound the public ip and private ip of the proxy server on port 80 and set the default backend to a variable called web_servers.  once wihin backend web_servers I set the balancing to round robin, set it to ignore cookies, set it to a maximum of 20 connections, and set up 2 servers named server1 and server2 with the 2 other aws instances ip's.
4. I used: sudo systemctl reload haproxy.service
5. I used the lecture on 11/8 and https://www.haproxy.com/blog/the-four-essential-sections-of-an-haproxy-configuration/

## webserver config

###
1. sudo apt install -y apache2
2. setting up a virtual host required me to make a directory at /var/www/cskIIproject5 (my domain). After that I was able to add the index.html that we were given inside the cskIIproject5 dir. then I set up a config file /etc/apache2/sites-available/cskProject5.conf 
3. I set the the ownership to the $USER environment variable. then I had to set the file permissions to 755. after that I used my .conf file to set the servername, serveralias, and documentroot.  after that you must enable your config using a2ensite and disable the default config using a2dissite 000-default.conf.  checked the config using apache2ctl config test, and then I was ready to restart apache.
4. I restarted the server using sudo systemctl restart apache2
5. I used https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04 to set up apache.
test
