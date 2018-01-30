# Getting Started with Solr 7
## Install JAVA 8
1.1 Visit Oracle JDK download [page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html), look for RPM version.

1.2 Copy the download link of jdk-8u102-linux-x64.rpm and wget it.

```$ pwd```
```/home/ec2-user```

```$ wget --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u161-b12/2f38c3b165be4555a1fa6e98c45e0808/jdk-8u161-linux-x64.rpm```

1.3 sudo yum localinstall jdk-8u161-linux-x64.rpm
Now the JDK should be installed at /usr/java/jdk1.8.0_161
```[ec2-user@ip-10-0-165-144 ~]$ ls -al /usr/java/```
```total 0```
```drwxr-xr-x.  3 root root  55 Jan 30 21:11 .```
```drwxr-xr-x. 14 root root 167 Dec 20 00:27 ..```
```lrwxrwxrwx.  1 root root  16 Jan 30 21:11 default -> /usr/java/latest```
```drwxr-xr-x.  9 root root 268 Jan 30 21:11 jdk1.8.0_161```
```lrwxrwxrwx.  1 root root  22 Jan 30 21:11 latest -> /usr/java/jdk1.8.0_161```

1.4 Verification

```$ java -version```
```[ec2-user@ip-10-0-165-144 ~]$ java -version```
```java version "1.8.0_161"```
```Java(TM) SE Runtime Environment (build 1.8.0_161-b12)```
```Java HotSpot(TM) 64-Bit Server VM (build 25.161-b12, mixed mode)```

```AVA_HOME Environment Variables```
```This is good practice to set the JAVA_HOME environment variable.```

1.5 Edit the .bash_profile, and append the export JAVA_HOME at the end of the file, for example :

```.bash_profile```
```# Get the aliases and functions```
```if [ -f ~/.bashrc ]; then```
```	. ~/.bashrc```
```fi```

```# User specific environment and startup programs```

```# User specific environment and startup programs```
```export JAVA_HOME=/usr/java/jdk1.8.0_102/```
```export JRE_HOME=/usr/java/jdk1.8.0_102/jre```

```PATH=$PATH:$HOME/.local/bin:$HOME/bin:$JAVA_HOME/bin```

```export PATH```

1.6 Test the $JAVA_HOME and $PATH

```$ source .bash_profile```

```$ echo $JRE_HOME```
```/usr/java/jdk1.8.0_161/jre```

$ echo $JAVA_HOME
/usr/java/jdk1.8.0_161/

$ echo $PATH
/...:/usr/local/bin:/usr/X11R6/bin:/home/mkyong/bin:/usr/java/jdk1.8.0_161//bin```

## Install Solr 7
```pwd /home/ec2-user/solr7```
```1.1 download Solr  wget http://apache.claz.org/lucene/solr/7.2.1/solr-7.2.1.tgz```

To keep things simple for now, extract the Solr distribution archive to your local home directory, for instance on Linux, do:

```cd ~/```
```[ec2-user@ip-10-0-165-144 ~]$ pwd```
```/home/ec2-user```
```tar zxf solr-7.0.0.tgz```
Once extracted, you are now ready to run Solr using the instructions provided in the Starting Solr section below.```

## Starting Solr
```bin/solr start```

```cd solr-7.2.1/```
```[ec2-user@ip-10-0-165-144 solr-7.2.1]$ pwd```
```/home/ec2-user/solr-7.2.1```
```ec2-user@ip-10-0-165-144 solr-7.2.1]$ bin/solr start```
```NOTE: Please install lsof as this script needs it to determine if Solr is listening on port 8983.```

```Started Solr server on port 8983 (pid=12024). Happy searching!```
## Access Solr at 8983
'http://ec2-54-190-42-115.us-west-2.compute.amazonaws.com:8983/solr/#/'




