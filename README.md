# Hadoop

https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-common/SingleCluster.html

```sh
cd hadoop_workspace
docker build -t hadoop_demo .
docker run --network=host -it hadoop_demo
```

In the container run:
```sh
./hadoop-3.3.1/sbin/start-all.sh
```

If you can't ssh to localhost, run the following from the apache docs:
```sh
ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
chmod 0600 ~/.ssh/authorized_keys
```

To check that all of the services are running, use jps (Java Virtual Machine Process Status Tool):
```sh
jps
```
output:
```
77907 SecondaryNameNode
77810 DataNode
78098 NodeManager
78005 ResourceManager
5716 Jps
73735 JobHistoryServer
77721 NameNode
56297 Kafka
362 
78271 RunJar
```
