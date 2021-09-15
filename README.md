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
