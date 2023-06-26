#A static route is a route that is entered manually by the network administrator in order to create a route that is reliable and safe.
There are four different static routes used in this activity: a recursive static route; a directly attached static route; a fully specified static route; and a default route.



 Which command is used to configure IPv6 static routes?
ipv6 route [network/prefix] [exit interface/next hop address]



Configure IPv6 Static and Default Routes
Step 1: Enable IPv6 routing on all routers.
 #ipv6 unicast-routing


Configure recursive static routes on R1.

Configure an IPv6 recursive static route to every network not directly connected to R1.

#ipv6 route 2001:DB8:1:2::/64 2001:DB8:1:A001::2




Step 3: Configure a directly attached and a fully specified static route on R2.
a. Configure a directly attached static route from R2 to the R1 LAN.

#ipv6 route 2001:DB8:1:1::/64 Serial0/0/0


Configure a fully specific route from R2 to the R3 LAN.

#ipv6 route 2001:DB8:1:3::/64 Serial0/0/1 2001:DB8:1:A002::2


Configure a default route on R3.
Configure a recursive default route on R3 to reach all networks not directly connected.

ipv6 route ::/0 2001:DB8:1:A002::1


Verify static route configurations.
a. Which command is used to verify the IPv6 configuration of a PC from the command prompt? 
	ipv6config

b. Which command displays the IPv6 addresses configured on a router’s interface? 
	show ipv6 interface brief
c. Which command displays the contents of the IPv6 routing table? 
	show ipv6 route
