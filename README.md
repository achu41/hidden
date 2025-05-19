Program 1:
$ sudo addgroup hadoop_  
// Adding group hadoop_ done.

$ sudo adduser --ingroup hadoop_ hduser_  
// Adding user hduser_ to group hadoop_ done. User account created.

$ sudo adduser hduser_ sudo  
// Added hduser_ to group sudo.

$ su - hduser_  
// Switched to user hduser_.

$ ssh-keygen -t rsa -P ""  
// SSH key pair generated with empty passphrase.

$ cat $HOME/.ssh/id_rsa.pub >> $HOME/.ssh/authorized_keys  
// Public key added to authorized_keys for passwordless SSH.

$ ssh localhost  
// Logged in to localhost without password.

$ sudo apt-get purge openssh-server  
// OpenSSH server package removed.

$ sudo apt-get install openssh-server  
// OpenSSH server installed successfully.


Program 2: 
$ sudo apt update  
// Package list updated.

$ sudo apt install openjdk-8-jdk -y  
// Java 8 JDK installed successfully.

$ java -version; javac -version  
// Displaying Java and javac version.

$ sudo adduser hdoop  
// Added user hdoop. Prompts for password.

$ su - hdoop  
// Switched to user hdoop.

$ ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa  
// SSH key generated with no passphrase.

$ cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys  
// Public key added to authorized keys.

$ chmod 0600 ~/.ssh/authorized_keys  
// Permissions for authorized_keys set to 600.

$ ssh localhost  
// SSH login to localhost successful without password.

$ wget https://downloads.apache.org/hadoop/common/hadoop-3.2.1/hadoop-3.2.1.tar.gz  
// Hadoop 3.2.1 tarball downloaded.

$ tar xzf hadoop-3.2.1.tar.gz  
// Extracted Hadoop package.



Program 3:
$ ./hadoop-daemon.sh start namenode  
// Namenode started.

$ ./hadoop-daemon.sh start datanode  
// Datanode started.

$ ./yarn-daemon.sh start resourcemanager  
// ResourceManager started.

$ ./yarn-daemon.sh start nodemanager  
// NodeManager started.

$ ./mr-jobhistory-daemon.sh start historyserver  
// JobHistoryServer started.

$ jps  
// Displays running Java processes (e.g., NameNode, DataNode, ResourceManager, etc.).



Program 4: 
$ hdfs dfs -appendToFile localfile.txt /user/hdoop/targetfile.txt  
// Contents from localfile.txt appended to /user/hdoop/targetfile.txt in HDFS.

$ hdfs dfs -cat /user/hdoop/targetfile.txt  
// Displays the contents of the file from HDFS.

$ hdfs dfs -chgrp hadoopgrp /user/hdoop/targetfile.txt  
// Group of the file changed to hadoopgrp.

$ hdfs dfs -chmod 755 /user/hdoop/targetfile.txt  
// Permissions set to rwxr-xr-x.

$ hdfs dfs -chown hdoop:hadoopgrp /user/hdoop/targetfile.txt  
// Owner changed to hdoop and group to hadoopgrp.



Program 5: 
$ hadoop jar wordcount.jar /input /output  
// Hadoop MapReduce WordCount job executed.

$ hadoop fs -cat /output/part-r-00000  
// Displays output of MapReduce job (word count results).
