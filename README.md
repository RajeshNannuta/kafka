# kafka
kafka for begineers

how to setup kafka in windows/linux environment

# Prerequisite

For windows user:

1. Download latest version of java (http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) or (http://www.oracle.com/technetwork/java/javase/downloads/java-archive-javase8-2177648.html)
2. Download latest and stable version of zookeeper(http://www-eu.apache.org/dist/zookeeper/stable/) 
3. Download latest version of kafka (https://www.apache.org/dyn/closer.cgi?path=/kafka/0.11.0.0/kafka_2.12-0.11.0.0.tgz as am using scala 2.12) else you can download it from(https://kafka.apache.org/downloads)

# how to configure:

# FIRST STEP : Installing java & setting up the Environmental Variables

Install java from the Extracted file

Change the installation directory to any path without spaces in folder name. Ex C:\Java\jre1.8.0_xx\. (By default it will be C:\Program Files\Java\jre1.8.0_xx) 

Set the environmental variables:

open system environment variables dialogue by opening Control Panel -> System -> Advanced system settings -> Environment Variables…
Hit New… button in User variables section then type JAVA_HOME in Variable name & give your jre path in Variable value .make sure that you are giving the exact jre.1.8 path.

Edit Path variable in the “System Variable” section in “Environment Variables” dialogue box you just opened.
Edit the path and type “;%JAVA_HOME%\bin” .

To check weather you have installed latest version of java . Type "java -version" in command prompt.it should display like this
    
    java version "1.8.0_112"
    Java(TM) SE Runtime Environment (build 1.8.0_112-b15)
    Java HotSpot(TM) 64-Bit Server VM (build 25.112-b15, mixed mode)
If you are unable see this output. Try to re-install setup again.

# SECOND STEP : Installing and setting up ZOOKEEPER

unzip the file that you have downloaded.

create a folder in c: drive as zookeeper-3.4.10 and move the extracted files into that folder.

Goto your zookeeper config directory. For me its C:\zookeeper-3.4.10\conf

Rename file “zoo_sample.cfg” to “zoo.cfg”

Open zoo.cfg and edit dataDir=/tmp/zookeeper to dataDir=C:\zookeeper-3.4.10\data

if needed You can change the default zookeeper port in zoo.cfg file (Default port 2181).

Environmental variables:

Add in System Variables ZOOKEEPER_HOME = C:\zookeeper-3.4.10
Edit System Variable named “Path” add ;%ZOOKEEPER_HOME%\bin;


# THIRD STEP: Kafka installation

unzip the file.Go to your Kafka config directory. For me its C:\kafka_2.12-0.11.0.0\config then Edit file “server.properties

edit line “log.dirs=/tmp/kafka-logs” to “log.dir= C:\kafka_2.12-0.11.0.0\kafka-logs”

If your zookeeper is running on some other machine or cluster you can edit “zookeeper.connect=localhost:2181” to your custom IP & port. Also Kafka port & broker.id are configurable in this file. Leave other settings as it is.

Your Kafka will run on default port 9092 & connect to zookeeper’s default port which is 2181.




for linux users:

1.Install java latest version using command
         for centos : use sudo yum install java-1.8.0-openjdk.x86_64.
         for ubuntu : use sudo apt-get install openjdk-8-jdk

2.Download zookeeper using following command wget http://www-eu.apache.org/dist/zookeeper/stable/zookeeper-3.4.10.tar.gz 

3.Download kafka : wget http://www-eu.apache.org/dist/kafka/0.11.0.0/kafka_2.12-0.11.0.0.tgz 
 
 # how to configure JAVA and KAFKA in centos
 
 # Java configaration
 after installing java set the environmental variables.
 we can set environmental veriables for every user by editing /etc/profile file
 
 To edit that file type: sudo vi /etc/profile in terminal
 
 Add this content at the bottom of the file.
 export JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk.x86_64
 export JRE_HOME=/usr/lib/jvm/jre 
 
 make sure that u are giving the exact jre & jdk path.before configuring check throghly.
 
 Save and quit: :wq 
 
 Reload the profile to put your changes into effect:
 type : source /etc/profile
 
 # kafka configuration
 unzip the tar file and move contents to preffered location using
 
 tar -xvf kafka_2.11-0.9.0.1.tgz 
 sudo mv kafka_2.11-0.9.0.1 /opt
 
 To configure kafka use
 vi bin/kafka-server-start.sh 


   
   
