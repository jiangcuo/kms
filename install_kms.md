# 安装KMS服务

一键脚本

`wget --no-check-certificate https://github.com/teddysun/across/raw/master/kms.sh && chmod +x kms.sh && ./kms.sh`

查看端口

`netstat -nxtlp | grep 1688`

```
# 启动
/etc/init.d/kms start

# 停止
/etc/init.d/kms stop

# 重启
/etc/init.d/kms restart

# 状态
/etc/init.d/kms status

# 卸载
./kms.sh uninstall
```
help

<https://teddysun.com/530.html>