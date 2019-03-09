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

#Intitializing Scala interpreter ...
#Spark Web UI available at http://kuns-mbp.lan:4040
#SparkContext available as 'sc' (version = 2.4.0, master = local[*], app id = local-1552095553143)
#SparkSession available as 'spark'
```
