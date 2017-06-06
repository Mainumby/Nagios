# Nagios
Commands needed for Nagios Core install on Centos 7
    1  yum repolist
    2  ping 8.8.8.8
    3  ping google.com
    4  yum update
    5  ip config
    6  ifconfig
    7  cat /etc/networks/
    8  ls
    9  cd /etc/networks/
   10  yum repolist
   11  ifconfig -a
   12  man chkconfig
   13  man chkconfig --list
   14  cd /etc/networks 
   15  cd /etc/
   16  ls
   17  cat networks 
   18  yum update
   19  cd /etc/sysconfig/network
   20  cd /etc/sysconfig/network-scripts/
   21  ls
   22  nmcli d
   23  cat ifcfg-eth0 
   24  systemctl restart network
   25  yum update
   26  cd ..
   27  cd..
   28  cd ..
   29  setenforce 0
   30  yum install nano 
   31  nano /etc/selinux/config 
   32  yum install httpd php php-cli glibc glibc-common gd gd-devel net-snmp openssl-devel wget unzip -y
   33  groupadd nagcmd
   34  usermod -a -G nagcmd nagios
   35  usermod -a -G nagcmd apache
   36  cd /tmp/
   37  wget
   38  wget https://assets.nagios.com/downloads/nagioscore/releases/nagios-4.1.1.tar.gz
   39  wget http://www.nagios-plugins.org/download/nagios-plugins-2.1.1.tar.gz
   40  tar zxf nagios-4.1.1.tar.gz 
   41  tar zxf nagios-plugins-2.1.1.tar.gz 
   42  cd nagios-4.1.1
   43  exit
   44  ./configure --with-command-group=nagcmd
   45  yum install gcc
   46  ./configure --with-command-group=nagcmd
   47  make all
   48  make install
   49  make install-init
   50  make install-config
   51  make install-commandmode
   52  make install-webconf
   53  htpasswd -c /usr/local/nagios/etc/htpasswd.users nagiosadmin
   54  cd /tmp/nagios-plugins-2.1.1
   55  ./configure --with-nagios-user=nagios --with-nagios-group=nagios --with-openssl
   56  make all
   57  make install
   58  service httpd start
   59  service nagios start
   60  history
   61  history >> comandos.txt
