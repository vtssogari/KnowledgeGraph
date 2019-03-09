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

// Neo4J connector
launcher.conf.set("spark.neo4j.bolt.url", "bolt://127.0.0.1:7687")
launcher.conf.set("spark.neo4j.bolt.user", "neo4j")
launcher.conf.set("spark.neo4j.bolt.password", "neo4j")

launcher.num_executors = 2
launcher.executor_cores = 2
launcher.driver_memory = '4g'
launcher.packages = ["neo4j-contrib:neo4j-spark-connector:2.4.0-M6"]



#Intitializing Scala interpreter ...
#Spark Web UI available at http://kuns-mbp.lan:4040
#SparkContext available as 'sc' (version = 2.4.0, master = local[*], app id = local-1552095553143)
#SparkSession available as 'spark'
```
