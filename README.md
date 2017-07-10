# kafka
kafka for begineers

how to setup kafka in windows/linux environment

# Prerequisite

For windows user:

1. Download latest version of java (http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) or (http://www.oracle.com/technetwork/java/javase/downloads/java-archive-javase8-2177648.html)
2. Download latest and stable version of zookeeper(http://www-eu.apache.org/dist/zookeeper/stable/) 
3. Download latest version of kafka (https://www.apache.org/dyn/closer.cgi?path=/kafka/0.11.0.0/kafka_2.12-0.11.0.0.tgz as am using scala 2.12) else you can download it from(https://kafka.apache.org/downloads)

# how to configure:

First step : Installing java & setting up the Environmental Variables

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


   
   
