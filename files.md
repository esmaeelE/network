# Unix like

* ```/etc/services```

For each service this file specifies the service’s well-known port number and notes whether the service is available as a TCP or
UDP service.
```
ssh		22/tcp				# SSH Remote Login Protocol
telnet		23/tcp
smtp		25/tcp		mail
time		37/tcp		timserver
time		37/udp		timserver
whois		43/tcp		nicname
tacacs		49/tcp				# Login Host Protocol (TACACS)
tacacs		49/udp
domain		53/tcp				# Domain Name Server
```

# Windows ```protocols```

Location: ```C:\Windows\System32\drivers\etc```

```
#
# This file contains the Internet protocols as defined by various
# RFCs.  See http://www.iana.org/assignments/protocol-numbers 
#
# Format:
#
# <protocol name>  <assigned number>  [aliases...]   [#<comment>]

ip         0     IP           # Internet protocol
icmp       1     ICMP         # Internet control message protocol
ggp        3     GGP          # Gateway-gateway protocol
tcp        6     TCP          # Transmission control protocol
egp        8     EGP          # Exterior gateway protocol
pup        12    PUP          # PARC universal packet protocol
udp        17    UDP          # User datagram protocol
hmp        20    HMP          # Host monitoring protocol
xns-idp    22    XNS-IDP      # Xerox NS IDP
rdp        27    RDP          # "reliable datagram" protocol
ipv6       41    IPv6         # Internet protocol IPv6
ipv6-route 43    IPv6-Route   # Routing header for IPv6
ipv6-frag  44    IPv6-Frag    # Fragment header for IPv6
esp        50    ESP          # Encapsulating security payload
ah         51    AH           # Authentication header
ipv6-icmp  58    IPv6-ICMP    # ICMP for IPv6
ipv6-nonxt 59    IPv6-NoNxt   # No next header for IPv6
ipv6-opts  60    IPv6-Opts    # Destination options for IPv6
rvd        66    RVD          # MIT remote virtual disk
```
