# zabbix tempates
## Vplex Template
### configuration in Vplex
  * For PULLing info from VPLEX (snmp GET, not necessary for traps):

        snmp-agent configure                     # MUST be run as service

        snmp-agent start

        snmp-agent status

        snmp-agent unconfigure
        
  * For VPLEX SNMP traps generated by call-home  events:  (default port is 162)

        cd /notifications/call-home

        snmp-trap create  <trap-name>

        cd /notifications/call-home/snmp-traps/<trap_name>

        set remote-host  <IP Address>   # IP address of server receiving traps

        set community-string  <string>  # default is public

        set started true

        notifications call-home test will generate a test trap
### Change SNMP Community
### Done!
----------------------------------
中文用户可能参考本人订阅号上的说明：
https://mp.weixin.qq.com/s?__biz=MzUwOTc0MjQzMQ==&mid=2247483794&idx=1&sn=575bd4ffc8974c22cff00527836230fa&chksm=f90cdda2ce7b54b40dec9b1972ce4b783818611cf84447800a52c12f60b16973a927ed0fc192&token=569269806&lang=zh_CN#rd
