## Network related questions

- TCP

  - Three way handshake:

    |          Client           |          |          Server         |
    |---------------------------|----------|-------------------------|
    |Send SYN(seq=x)            | -------> | receive SYN(seq=x)      |
    |receive SYN(seq=y, ACK=x+1)| <------- | send SYN(seq=y, ACK=x+1)|
    |send ACK(ACK=y+1)          | <------- | receive ACK(ACK=y+1)    |	

  - What's inside a TCP packet?
    source port, destination port, sequence number, ack number(if ACK set), data offset, reserved, flags, windows size, checksum...etc.

- UDP

  - Connectionless
  - Perform error checking but also drop large amount of packets
  - fast
  - no ack and no handshake
  - broadcast and multcast supported

- DHCP
  - Dynamically allocate network configuation data, such as IP, subnet mask, default gateway IP address, DNS IP address, lease time, ...etc
- NAT
  - Allow private IP to connect the public network
  - Hide the local network IP, all the outsource IP will be the same
  - Will distrubute the insource packets to specific local IP by port
- IGMP(nternet Group Management Protocol)
  - IGMP is a communications protocol used by hosts and adjacent routers on IPv4 networks to establish multicast group memberships
  - Multicast management on IPv6 networks is handled by [Multicast Listener Discovery](https://en.wikipedia.org/wiki/Multicast_Listener_Discovery) (MLD)
- ICMP
  - used in `traceroute` and `ping`
  - ICMP packet is encapsulated in an IPv4 packet.
