# maven
yum install wget


[root@localhost maven]# wget https://downloads.apache.org/maven/maven-3/3.8.1/binaries/apache-maven-3.8.1-bin.tar.gz


[root@localhost maven]# ls -lart
total 9316
-rw-r--r--. 1 root root 9536838 Mar 30 18:41 apache-maven-3.8.1-bin.tar.gz
dr-xr-x---. 4 root root     160 Apr 16 04:38 ..
drwxr-xr-x. 3 root root      69 Apr 16 05:02 .
drwxr-xr-x. 6 root root      99 Apr 16 05:02 apache-maven-3.8.1
[root@localhost maven]# cd /etc/profile.d

[root@localhost profile.d]# pwd
/etc/profile.d


[root@localhost profile.d]# cat /etc/profile.d/maven.sh
#apache maven environment variable
#
#
export M2_HOME=/root/maven/apache-maven
export PATH=${M2_HOME}/bin:${PATH}
[root@localhost profile.d]#


[root@localhost profile.d]# mvn --version
Apache Maven 3.8.1 (05c21c65bdfed0f71a2f2ada8b84da59348c4c5d)
Maven home: /root/maven/apache-maven
Java version: 1.8.0_282, vendor: Red Hat, Inc., runtime: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.282.b08-1.el7_9.x86_64/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "3.10.0-957.el7.x86_64", arch: "amd64", family: "unix"

