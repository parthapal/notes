# notes
amazon linux ec2
------------------
oracle jdk 8

1. yum update -y
2. yum remove java-1.7.0-openjdk -y (remove already installed java 1.7)
3. wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u112-b15/jdk-8u112-linux-x64.rpm
4. rpm -Uvh jdk-8u112-linux-x64.rpm
5. alternatives --install /usr/bin/java java /usr/java/jdk1.8.0_112/jre/bin/java 20000
6. alternatives --install /usr/bin/jar jar /usr/java/jdk1.8.0_112/bin/jar 20000
7. alternatives --install /usr/bin/javac javac /usr/java/jdk1.8.0_112/bin/javac 20000
8. alternatives --install /usr/bin/javaws javaws /usr/java/jdk1.8.0_112/jre/bin/javaws 20000
9. alternatives --set java /usr/java/jdk1.8.0_112/jre/bin/java
10. alternatives --set javaws /usr/java/jdk1.8.0_112/jre/bin/javaws
11. alternatives --set javac /usr/java/jdk1.8.0_112/bin/javac
12. alternatives --set jar /usr/java/jdk1.8.0_112/bin/jar


tomcat 8

1. cd /opt/
2. wget http://ftp.itu.edu.tr/Mirror/Apache/tomcat/tomcat-8/v8.5.14/bin/apache-tomcat-8.5.14.tar.gz
3. tar -xvf apache-tomcat-8.5.14.tar.gz
4. edit server.xml change ports to 80 & 443
5. cd /opt/apache-tomcat-8.5.14/bin
6. ./startup.sh 

mysql-server

1. yum install mysql-server
2. service mysqld start
3. mysql_secure_installation

mysql -u root -p


mysql>create database gallery;
mysql>grant all privileges on gallery.* to 'ryan'@'from_host' identified by "GanD1do"; 
mysql>flush privileges;

