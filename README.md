
Hadoop
-------
@echo off
copy file system to hdfs
hdfs dfs -copyFromLocal /Users/Dimbisoa/people.json  /destination
show hdfs file system
hdfs dfs -ls /destination
start-all.cmd
start-yarn.cmd
jps

Storm
----
C:\storm\bin>python storm.py nimbus Supervisor
C:\storm\bin>python storm.py supervisor Storm UI
C:\storm\bin>python storm.py ui

Kafka
-----
rem "%JAVA_HOME% sans bin folder."
cd "C:\"
cd kafka
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
.\bin\windows\kafka-server-start.bat .\config\server.properties
cd "C:\"
cd kafka\bin\windows
rem "create kafka topic"
kafka-topics.bat --create --topic test --bootstrap-server localhost:9092
rem "create kafka producer"
kafka-console-producer.bat --broker-list localhost:9092 --topic test
rem "create kafka consumer"
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning
exit

Zeppelin
--------
Go to bin home folder zeppelin.
run zeppelin.bat
