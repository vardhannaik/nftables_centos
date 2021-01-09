# nftables_centos
Example for nftables for Centos

Based on https://cryptsus.com/blog/setting-up-nftables-firewall.html

Some concepts for this template
1) IPV6 incoming stopped except for ICMP6, IPV6 outgoing allowed
2) SMTP 25 is blocked by ISP, for split delivery don't use port but IP
3) FIREWALL used in include file to reject early
4) Interplay of meta data accept from ip, ip6 to inet family
5) state capture in inet for IPV6 which was not possible in ip6 family

$ sudo systemctl restart nftables && systemctl status nftables && nft list ruleset
