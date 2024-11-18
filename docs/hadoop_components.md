# Notes
Use JDK 11 in computer for stability and all commands in administrator mode.
For testing command if run successfully, you must run command "jps".
Safemode in Apache Hadoop is a maintenance state of NameNode, during which NameNode 
doesn't allow any modifications to the file system. In Safemode, 
HDFS cluster is in read-only and doesn't replicate or delete Data Blocks.
netsh advfirewall firewall add rule name="Zookeeper Port 2181" dir=in action=allow protocol=TCP localport=2181
## Run Hadoop
start-dfs.cmd
## Run Yarn
start-yarn.cmd
## Set Hadoop to safe mode
hdfs dfsadmin -safemode leave
## Run HBase
start-hbase.cmd