# apache-struts2-CVE-2017-5638
Demo Application and Exploit

To build a compromised host in AWS use the following in Userdata, with port 8080 open:
#!/bin/bash
sudo yum -y update
sudo yum -y install git tomcat7
cd /home/ec2-user/
sudo git clone https://github.com/belialboy/apache-struts2-CVE-2017-5638.git
sudo cp apache-struts2-CVE-2017-5638/struts2-showcase-2.3.12.war /var/lib/tomcat7/webapps
sudo service tomcat7 restart

Sample Apache Struts2 App 

Struts2-showcase: https://mvnrepository.com/artifact/org.apache.struts/struts2-showcase/2.3.12

Exploit Reference: https://github.com/rapid7/metasploit-framework/issues/8064
