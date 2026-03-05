# Enterprise-Security-Homelab
The general architecture of the lab is such that:

Internet
|
Proxmox
|
OPNsense (firewall / gateway / IDS)
|
Internal LAN (vnet)
	|-Windows server (AD, DNS, File Share)
	|-Ubuntu server (web apps + logs)
	|-Windows 11 User machine
	|-Kali Linux (attacker - external / untrusted vlan)


This to effectively discriminate the inside and outside of the network given a virtualized environment as opposed to a server rack and big network switchboard. Proxmox was chosen as the hypervisor in order to closely emulate real-world enterprise virtualization. Learning virtualization through this lens allows for a better critical analysis of system architecture.
