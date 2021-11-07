```shell
tar -zxvf jdk-8u202-linux-x64.tar.gz
```

```
vi /etc/profile
```

```shell
export JAVA_HOME=/usr/local/jdk1.8.0_301
export JRE_HOME=$JAVA_HOME/jre
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
export PATH=$JAVA_HOME/bin:$PATH
```

```shell
source /etc/profile
```



