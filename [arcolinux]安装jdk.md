* 下载jdk包（选择对应的版本）

  https://www.oracle.com/java/technologies/downloads/archive/

* 解压安装包并移动到合适的位置（服务器上可移动到`/usr/local`）

  ```shell
  tar -zxvf jdk-8u202-linux-x64.tar.gz
  ```

* 配置环境变量（服务器上是`/etc/profile`）

  ```shell
  nvim ~/.profile
  ```

  ```shell
  export JAVA_HOME=/home/luis/DevelopmentTools/jdk1.8.0_202
  export JRE_HOME=$JAVA_HOME/jre
  export PATH=$JAVA_HOME/bin:$PATH
  export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
  ```

  jre可以不设置

* 刷新

  ```shell
  source ~/.profile
  ```

* 重启（有时候需要重启才能生效）

  ```shell
  reboot
  ```

注：上述环境变量是在bash的环境下配置的，如果使用fish shell，那么也可以根据fish shell环境变量的配置方法进行配置（因为fish shell不兼容bash），如果在fish shell中配置，那么最终在bash和fish都可以使用java了。



fish环境变量配置方法：

```shell
nvim ~/.config/fish/config.fish
```

除PATH之外，可按照bash风格用:来分割多个值，但在PATH中不能用:来分割，必须用空格分割

```shell
set -x JAVA_HOME /home/luis/DevelopmentTools/jdk1.8.0_202
set -x JRE_HOME {$JAVA_HOME}/jre
set -x PATH {$JAVA_HOME}/bin {$PATH}
set -x CLASSPATH .:{$JAVA_HOME}/lib/dt.jar:{$JAVA_HOME}/lib/tools.jar
```

jre可以不设置

```shell
source ~/.config/fish/config.fish
```

```shell
reboot
```















