# Ubuntu-lotserver
```wget xiaofd.github.io/ruisu.sh && bash ruisu.sh```  
注意：

安装完会自动重启 正常现象 重启后就安装好了锐速，可以使用 ps aux | grep appex 来检测是否运行
如果锐速没有自动安装可以使用 bash /appex/appexinstall.sh 来安装
没有任何多余的判断，**非ubuntu16.04和ubuntu14.04请勿运行**
锐速使用 Vicer大佬 的 moeclub.org 给出的 lotserver 一键包  
## 附上 16.04 降低内核版本的方法
上面16.04使用的是最新内核，如果有需求可以按照下面方法手动切换旧版本内核，然后自行安装对应版本的锐速即可。  
```sudo cp /etc/apt/sources.list /etc/apt/sources.list_bak
 
echo "deb http://security.ubuntu.com/ubuntu trusty-security main" >> /etc/apt/sources.list
 
sudo apt-get update
 
sudo apt-get install linux-image-extra-3.16.0-43-generic
 
dpkg -l | grep 3.16.0-43-generic
 
vi /etc/default/grub
"Advanced options for Ubuntu>Ubuntu, with Linux 3.16.0-43-generic"
 
update-grub
reboot```
