# GCP
注册谷歌云 https://console.cloud.google.com/freetrial?referralId=70215fed64754b8b91729319a16ef599 快捷通道可能有额外奉送金额哦大家可以试试！

1. GCP创建VM实例
    

2.创建防火墙规则
    VPC网络→防火墙规则→创建防火墙规则

3. 打开VM实例SSH页

4. 获取管理员权限
    命令：sudo -i

5. 安装V2Ray
    1）一键安装：
bash <(curl -s -L https://233v2.com/v2ray.sh)

要求：Ubuntu 16+ / Debian 8+ / CentOS 7+ 系统
推荐使用 Debian 9 系统，脚本会自动启用 BBR 优化。
不推荐使用 Debian 8 系统，因为 Caddy 申请证书可能会出现一些莫名其妙的问题

如果提示 curl: command not found ，那是因为你的 VPS 没装 Curl
ubuntu/debian 系统安装 Curl 方法: apt-get update -y && apt-get install curl -y
centos 系统安装 Curl 方法: yum update -y && yum install curl -y
安装好 curl 之后就能安装脚本了

安装完成后，输入 v2ray 即可管理 V2Ray

6. 配置BBR加速，配置完成后重启机器
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh"
chmod +x tcp.sh
./tcp.sh

安装后，执行lsmod | grep bbr，显示有bbrplus则开启成功
