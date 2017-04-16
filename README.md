Createing AWS Test project using **Maven multi module template project**

-> create an EC2 instance or use an existing instance.

-> If you don't have access rights on your newly created private key Use
   chmod 400 "privatekeypath"

-> connect from terminal or any ssh client using.
   ssh -i "privatekey" ec2-user@<amazon_ec2_instance_name.com>

-> Update packages on your ec2 instance using
   sudo yum update -y
   
-> Install tomcat on ec2 instance, Get a list of package available
   sudo yum list tomcat*
   
-> pick tomcat packages from the result of list command and execute
   sudo yum install tomcat-webapps tomcat-admin-webapps
   
-> verify java is installed on ec2 instance 
   java -version
