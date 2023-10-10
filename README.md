# SAM-AWS-demo-for-websitestatic


Create an EC2-instance  and login    ( i use RedHat  for this demo ) ypu can use any OS

Switch user to ROOT ==  <  sudo su  - >


Run  ==  <  yum  update -y  >

         <  yum  install git >

         < git clone  the repo URL>

         < cd to  the repo  >

         < yum install  httpd  -y >     #installing our apache web-server

NB OUR website can only be host when is found under this directory <  /var/www/html  >    if not it won't be host and it wont work. 
>  So we are going to copy all the files and folder of our application  file to < /var/www/html> 
>> LET see the files and folder we have ==

[root@ip-172-31-41-80 SAM-AWS-demo-for-websitestatic]# ls
assets  error  images  index.html  README.md
[root@ip-172-31-41-80 SAM-AWS-demo-for-websitestatic]#

         Let copy  the to  /var/www/html 

         <  cp   index.html  /var/www/html >         # NB  index.html  is just a single file that is y we didn't use < -r > flag
         <   cp   -r assets   /var/www/html >        # NB the < assests > folder/directory has other file in it so fo the < cp to work we have to pass <-r> >
         < cp   -r error   /var/www/html >        
          <  cp   -r images   /var/www/html  > 

Next to verify if the files were all copied ==  

  <   cd    /var/www/html  >  ==

  [root@ip-172-31-41-80 SAM-AWS-demo-for-websitestatic]# cd /var/www/html/
[root@ip-172-31-41-80 html]# ls
assets  error  images  index.html
===========================

Next for us to be able to access our Webside we need to < START APACHE ( httpd )> ===

 < systemctl start   httpd >


Them access the application  with the public IP-address 

================================================= 
