# WordCount Mapping with Redis

Simple program for counting words in text using Java Maping and Redis for reducing and output. This project uses ```Jedis``` java library for ```Redis```

# Run the program

## Step 1

Make sure you have installed redis-server and configured files redis.conf and then check if redis client is working with this command in terminal

```console
redis-cli
ping
```
If the answer will be PONG it means all is set up.

## Step 2

Check if ip in jar and your machine matches

```console
ip a
```

if not, than fix it in source code.
## Step 3

```console
hadoop fs -mkdir -p "hadoop/redis/input"
hadoop fs -copyFromLocal *.txt hadoop/redis/input/
hadoop jar wordCount.jar hadoop/redis/input/<name_of_textFile> hadoop/redis/output
```
