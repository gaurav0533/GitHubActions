what is HTTPD? 
HTTPD Daemon is a software program that runs in the background of a web server and waits for the incoming server request.
The Daemon answers the request automatically and servers the hypertext and multimedia documents over the internet using HTTPD
 Steps :
  install the package 
  yum install httpd
  httpd --version

  Config Location:
  /etc/httpd/conf/httpd.conf
  /var/www/html/index.html ( need to add this file )

  Logs :
  log var/log/httpd

  how to start service 
  systemctl start httpd

  cd /etc/httpd/conf
  less /etc/httpd/conf
  Document root - If request comes from browser will get responce from this location "/var/www/html"
  Error Log file - " logs/error_log" 

  cd /var/www
  cd html/ - go into this file and create new file with  vi index.html
  pwd 

  systemctl status httpd
  systemctl start httpd

  if page is not working check firewall status of our system 
   systemctl status firewalld.service
  yum install firewalld
  systemctl unmask firewalld
  systemctl enable firewalld
  systemctl start firewalld
   
  
  
