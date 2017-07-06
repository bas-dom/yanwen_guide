操作系统： ubuntu 16

apt-get install redis-server

修改用户名密码

修改允许远程访问

# 注册为服务，并设置开机启动 #
设置redis开机启动

修改redis.conf（/etc/redis下）

          #打开后台运行选项
         daemonize yes
         #设置日志文件路径
         logfile "/var/log/redis/redis.log"

编写脚本

        vim /etc/init.d/redis

```

#!/bin/sh
# chkconfig: 2345 10 90
# description: Start and Stop redis

PATH=/usr/bin
REDISPORT=6379
EXEC=/usr/bin/redis-server
REDIS_CLI=/usr/bin/redis-cli
PIDFILE=/var/run/redis.pid
CONF="/etc/redis/redis.conf"

case "$1" in
    start)
        if [ -f $PIDFILE ]
        then
            echo "$PIDFILE exists, process is already running or crashed."
        else
            echo "Starting Redis server..."
            $EXEC $CONF
        fi
        if [ "$?"="0" ]
        then
            echo "Redis is running..."
        fi
        ;;
    stop)
        if [ ! -f $PIDFILE ]
        then
            echo "$PIDFILE exists, process is not running."
        else
            PID=$(cat $PIDFILE)
            echo "Stopping..."
            $REDIS_CLI -p $REDISPORT SHUTDOWN
            while [ -x $PIDFILE ]
            do
                echo "Waiting for Redis to shutdown..."
                sleep 1
            done
            echo "Redis stopped"
        fi
        ;;
    restart|force-reload)
        ${0} stop
        ${0} start
        ;;
    *)
        echo "Usage: /etc/init.d/redis {start|stop|restart|fore-reload}"
        exit 1
esac

```

使用脚本启动服务
          开启redis： service redis start
          停止redis： service redis stop
          重启redis： service redis restart
         查看服务状态：service redis status
最后将机器关机，重新启动
         此时redis服务也启动了。

# 防火墙开启 #
ufw enable
ufw allow 22/tcp
ufw allow 6379/tcp

# 验证 #


 从web服务器进行命令 telnet **redis地址** 6379

出现telent连接成功提示代表没有问题