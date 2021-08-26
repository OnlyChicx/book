# Exchange network-name

+ 修改/etc/sysconfig/network-scripts/ifcfg-eth0

```shell
NAME=eth0        此处修改为#NAME=eno16777736
DEVICE=eth0      此处修改为#DEVICE=eno16777736
```

+ 修改配置文件名

> mv /etc/sysconfig/network-scripts/ifcfg-eth0 /etc/sysconfig/network-scripts/ifcfg-eno16777736 

+ 更改/etc/default/grub启动菜单传递给内核的参数，在GRUB_CMDLINE_LINUX变量中加入“net.ifnames=0 biosdevname=0”

```
GRUB_CMDLINE_LINUX="crashkernel=auto  net.ifnames=0 biosdevname=0 rhgb quiet"  #添加GRUB_CMDLINE_LINUX变量net.ifnames=0 biosdevname=0
```

+ grub2-mkconfig -o /boot/grub2/grub.cfg

+ 修改/etc/udev/rules.d/70-eno-fix.rules配置文件，加入如下行

```
SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="00:0c:29:81:69:0f", NAME="eno16777736"
```

+ 重启Centos7系统，完成网卡改名
