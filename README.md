#### Createing AWS Test project using ```Maven multi module template project``` ####
---

- create an EC2 instance or use an existing instance.

- If you don't have access rights on your newly created private key Use
   chmod 400 "privatekeypath"

- connect from terminal or any ssh client using.
   
   ssh -i "privatekey" ec2-user@<amazon_ec2_instance_name.com>

- Update packages on your ec2 instance using 

  sudo yum update -y
   
- Install tomcat on ec2 instance, Get a list of package available
   
   sudo yum list tomcat*
   
- pick tomcat packages from the result of list command and execute
   
   sudo yum install tomcat-webapps tomcat-admin-webapps
   
- verify java is installed on ec2 instance 
   
   java -version
   
- download oracle java using \n

curl -L -O -H "Cookie: oraclelicense=accept-securebackup-cookie" -k "https://edelivery.oracle.com/otn-pub/java/jdk/8u66-b17/jdk-8u66-macosx-x64.dmg"


- donwload tomcat using 

sudo curl -O http://mirror.cogentco.com/pub/apache/tomcat/tomcat-8/v8.5.13/bin/apache-tomcat-8.5.13.tar.gz

sudo mkdir /opt/tomcat && sudo tar -xf apache-tomcat-8.5.13.tar.gz -C /opt/tomcat

- make ec-user owner of tomcat installation directory.

sudo chown -R ec2-user tomcat

- make sure your instance's security group allows Inbound request at 8080 for TCP

<CATALINA_HOME>/bin/startup.sh

- Copy generated artifact i.e. war files using SCP commond 

```scp -i "path_to_private_key_file" path_to_war_file ec-user@<amazon_ec2_instance_name.com>:path_to_save_file_on_EC2_server```




#### Docker installation on AWS Reh hat 7 instance ####

---
> sudo yum install yum-utils

sudo yum-config-manager --enable rhui-REGION-rhel-server-extras

sudo yum install docker



