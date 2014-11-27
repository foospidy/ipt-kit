ipt-kit
=======

Bash scripts to help setup port redirects with iptables. This can be helpful when you want to run a process on a lower port but without elevated privileges (e.g. root). These scripts were created for running HoneyPy (https://github.com/foospidy/HoneyPy) on low ports. They are independent from HoneyPy so can be used for any purpose. They are just convenience scripts for modifing iptables, and have only been tested on Debian.

#### Scripts

`ipt` - display current iptables

`ipt_set_tcp` - set a tcp port redirect

`ipt_set_udp` - set a udp port redirect

`ipt_reset` - reset iptables (no rules)


#### Example Usage

`sudo ./ipt_set_tcp 22 10022`

`sudo ./ipt_set_tcp 22 10022 eth1`

#### Changes Surviving Reboot
After setting new rules or reseting rules, if you want the changes to survive a reboot use:

`ipt_survive_reboot`
