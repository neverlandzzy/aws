---
description: Virtual Private Cloud
---

# VPC

![](.gitbook/assets/screen-shot-2021-03-11-at-11.18.06-pm%20%281%29.png)

**3 sets of ip address reserved for private ip address ranges**

* 10.0.0.0 - 10.255.255.255 \(10/8 prefix\)
* 172.16.0.0 - 172.31.255.255 \(172.16/12 prefix\)
* 192.168.0.0 - 192.168.255.255 \(192.168/16 prefix\)

**1 Subnet = 1 Availability Zone**

* You **cannot** have a subnet stretched over multiple Availability Zones.
* You **can** have multiple subnets in the same Availability Zone.

**What can we do with a VPC**

* Launch instances into a subnet of your choosing
* Assign custom IP address ranges in each subnet
* Configure route tables between subnets
* Create internet gateway and attach it to your VPC
* Much better security control over your AWS resources
* Instance security groups
* Subnet network access control lists\(ACLs\)

**VPC Peering**

* Allows you to connect one VPC with another via a direct network route using private IP addresses
* Instances behave as if they were on the same private network
* You can peer VPCs with other AWS accounts as well as with other VPCs in the same account
* Peering is in a star configuration - 1 central VPC peers with 4 others \(No Transitive Peering\)
* You can peer between regions.

![VPC Peering](.gitbook/assets/screen-shot-2021-03-11-at-11.38.18-pm.png)

No Transitive Peering means \(instances in\) VPC B can talk to VPC A, VPC C can talk to VPC A, but VPC B cannot talk to VPC C.

