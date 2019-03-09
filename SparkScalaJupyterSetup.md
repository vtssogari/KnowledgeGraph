## install scala 
Mac
```
brew update
brew install scala

# ~/.bash_profile
export SCALA_HOME=/usr/local/opt/scala
export PATH=$PATH:$SCALA_HOME/bin:$PATH
export SCALA_VERSION=2.12.8
export ALMOND_VERSION=0.3.1
```

## install Almond

```
pip install spylon-kernel
# or
conda install -c conda-forge spylon-kernel

python -m spylon_kernel install


```

## Notebook
```
%%init_spark
launcher.conf.set("spark.neo4j.bolt.url", "bolt://localhost:7687")
launcher.conf.set("spark.neo4j.bolt.user", "")
launcher.conf.set("spark.neo4j.bolt.password", "")

launcher.num_executors = 2
launcher.executor_cores = 2
launcher.driver_memory = '4g'
launcher.packages = ["neo4j-contrib:neo4j-spark-connector:2.4.0-M6"]
```

```
spark

import org.neo4j.spark._

val neo = Neo4j(sc)

val rdd = neo.cypher("MATCH (n:Medicine) RETURN n as id ").loadRowRdd
rdd.count
```
