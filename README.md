Some Check_MK plugins from the internet. Tested / modified to function on Linux CentOS7

The plugins require to install check-mk-agent for check_mk server.
Official documentation https://mathias-kettner.de/checkmk_linuxagent.html
$ yum install check-mk-agent
Also install xinetd to use the check_mk_agent
$yum install xinetd

Modify the file /etc/xinetd.d/check-mk-agent, here you can set the IP address of the monitoring server
"only from = IP / Hostname"; Also check if the agent is enabled: "disable  = no"
Start and enable at boot xinetd.
$ systemctl enable xinetd ; systemctl start xinetd