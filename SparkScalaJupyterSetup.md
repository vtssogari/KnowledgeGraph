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
curl -Lo coursier https://git.io/coursier-cli
chmod +x coursier
./coursier bootstrap \
    -r jitpack \
    -i user -I user:sh.almond:scala-kernel-api_$SCALA_VERSION:$ALMOND_VERSION \
    sh.almond:scala-kernel_$SCALA_VERSION:$ALMOND_VERSION \
    -o almond
    
./almond --install


jupyter kernelspec list
```
