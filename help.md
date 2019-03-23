# CentOS7.6

## iptables

1. **first, you need to install iptables-service:**

~~~bash
yum install iptables-services
~~~

2. **find iptables config file:** 

~~~bash
/etc/sysconfig/iptables
~~~

3. **add a record to the file**

~~~vim
-A INPUT -p tcp -m state --state NEW -m tcp --dport 22 -j ACCEPT
~~~



~~~bash
  service iptables restart # restart iptables
 /bin/systemctl restart iptables.service # restart iptables
~~~

