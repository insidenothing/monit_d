avg_antivirus
=======


#[root@xxx init.d]# ps -e |grep avg
#27915 pts/0    00:00:06 avgd
#27927 pts/0    00:00:05 avgavid
#27937 pts/0    00:00:00 avgtcpd
#27942 pts/0    00:00:00 avgscand
#27968 pts/0    00:00:00 avgsched

#[root@xxx init.d]# nmap localhost
#Starting Nmap 5.51 ( http://nmap.org ) at 2014-04-29 10:07 EDT
#Nmap scan report for localhost (127.0.0.1)
#Host is up (0.000010s latency).
#Other addresses for localhost (not scanned): 127.0.0.1
#Not shown: 988 closed ports
#PORT      STATE SERVICE
#10024/tcp open  unknown

# AVG configuration changes
#avgcfgctl -w 'Default.tcpd.smtp.enabled=false'
#avgcfgctl -w 'Default.tcpd.milter.enabled=true'
#avgcfgctl -w 'Default.tcpd.milter.socket=inet:10024@localhost'
#avgcfgctl -w 'Default.tcpd.milter.verbosity=0'
#avgcfgctl -w 'Default.tcpd.spam.header.enabled=true'
#avgcfgctl -w 'Default.tcpd.parsing.mime_certification_enabled=true'

Reference---
http://www.howtoforge.com/avg-antivirus-for-linux-freebsd-plus-postfix-mail-server
