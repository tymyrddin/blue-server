# Introduction

## What?

Monitor traffic to and from a host, and only allow legitimate traffic.

## Why?

* Prevent unauthorised remote access, but while a firewall should block backdoor access via a Trojan, there is a chance that this can be bypassed.
* Block unsuitable or immoral content, but consider the ethics of reading private content to be able to do so.

## How?

* [iptables](iptables.md)
* [nftables](nftables.md)
* [UFW](ufw.md)
* [firewalld](firewalld.md)
* [FireHOL](firehol.md)
* [Packet filtering with I/O Control](pf.md)
* [Fail2ban](fail2ban.md)
* [SSHguard](sshguard.md)
* [WAF](waf.md)
* [Port spoofing](port-spoofing.md)

## Notes

* `Deny All` and then add exceptions to restrict access to everything except the specific services you need to remain open.
* Avoid using `ANY` in `Allow` rules. A rule where the service field is `ANY` can open up `65,535` attack vectors, I mean, TCP ports. 
* Document all rules and use comments for relevant information (purpose, service, users/servers/devices affected, permanent or temporary, name of person that added it) 
* Review proposed and changed firewall rules before implementation
* Consider a WAF. Mind that it requires a lot of support work because the defaults are all very strict. Users can not ven make linux documentation pages in a dokuwiki without getting thrown out.
