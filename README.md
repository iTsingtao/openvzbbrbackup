# openvzbbrbackup for OpenVZ
# 仅个人备份使用，以应对可能出现的原作者（扩软博客博主）受不可抗力删除项目的情况。

# Debian 7 x64、Ubuntu 14 x64、CentOS 6 x64 (Linux,Only support x64 OS，require glibc version 2.14 and higher)
# install way 1
wget -N --no-check-certificate https://raw.githubusercontent.com/Ache1123/openvzbbrbackup/master/ovz-bbr-installer.sh && chmod +x ovz-bbr-installer.sh && bash ovz-bbr-installer.sh
# install way 2
apt-get update   
apt-get install git -y   
git clone https://github.com/Ache1123/openvzbbrbackup   
cd openvzbbrbackup    
chmod +x ovz-bbr-installer.sh    
./ovz-bbr-installer.sh local  

# check OpenVZ-bbr statue 
ping 10.0.0.2

# speed up multiple ports
vi /usr/local/haproxy-lkl/etc/port-rules    
> 8800 or 8800-8810
   # choose one command to restart haproxy
   systemctl restart haproxy-lkl   
   service haproxy-lkl restart
   
# uninstall OpenVZ-BBR 	
./ovz-bbr-installer.sh uninstall
