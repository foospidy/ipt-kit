ipt-kit
=======

Bash scripts to help setup port redirects with iptables. This can be helpful when you want to run a process on a lower port but without elevated privileges (e.g. root). These scripts were created for running HoneyPy (https://github.com/foospidy/HoneyPy) on low ports. The are independent from HoneyPy so can be used for any purpose. All they do is make modifing iptables more convenient.

Scripts:

ipt - display current iptables

ipt_set_tcp - set a tcp port redirect

ipt_set_udp - set a udp port redirect

ipt_reset - reset iptables (no rules)


Example Usage:

sudo ./ipt_set_tcp 22 10022

sudo ./ipt_set_tcp 22 10022 eth1
