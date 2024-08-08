
- [SD-WAN](#SD-WAN)
- [Interface](#Interface)
- [step 0.5 Interface  Role](#step0.5InterfaceRole)
- [step 1 SD-WAN Zones](#step1SD-WANZones)
- [step 2 Performance SLAs](#step2PerformanceSLAs)
- [step 3  SD-WAN Rules](#step3SD-WANRules)


# SD-WAN
####  <a name='SD-WAN'></a>SD-WAN
   
####  <a name='Interface'></a>Interface

- the section sd-wan we are just foucus firewall 1 
![topology](image-sdwan/typology.png)

- make sure whether interface wan both 2 can connect to the internet.
![interfacewan](image-sdwan/interfacewan.png)


##  <a name='step0.5InterfaceRole'></a>step 0.5 Interface  Role
#### This step just gives a name and role to interface 

![rolewan1.png](image-sdwan/rolewan1.png)
![rolewan2.png](image-sdwan/rolewan2.png)
![shorolewan.png](image-sdwan/shorolewan.png)


##  <a name='step1SD-WANZones'></a>step 1 SD-WAN Zones
#### This step is the same as combination interface both WAN1 and WAN2 is Virtual-wan 

![click-virtualwanlink.png](image-sdwan/click-virtualwanlink.png)

![interfacemember.png](image-sdwan/interfacemember.png)


![create-int-wan1.png](image-sdwan/create-int-wan1.png)
![create-int-wan2.png](image-sdwan/create-int-wan2.png)

![addintface-invirtual-wan-link.png](image-sdwan/addintface-invirtual-wan-link.png)

![after-add-int.png](image-sdwan/after-add-int.png)

##  <a name='step2PerformanceSLAs'></a>step 2 Performance SLAs
#### This step is for creating performance measures, which we use for comparative performance between WAN1 and WAN2.


![create-sla.png](image-sdwan/create-sla.png)

![setting-sla.png](image-sdwan/setting-sla.png)

- It success
![sh-after-set-sla.png](image-sdwan/sh-after-set-sla.png)


##  <a name='step3SD-WANRules'></a>step 3  SD-WAN Rules
#### this step forces whether The application or destination out going to WAN1, WAN2, or load balance    

![create-rule.png](image-sdwan/create-rule.png)


##### 2 example rule
###### rule 1 for YouTube If the user in LAN uses the YouTube system, It select WAN at lowest SLA
###### rule 2 for Facebook If the user in LAN uses the Facebook system, It select WAN 1 because it's static

- Youtube rule
![sd-wan-youtube-lb.png](image-sdwan/sd-wan-youtube-lb.png)
- Facebook rule
![sd-wan-facebook-static.png](image-sdwan/sd-wan-facebook-static.png)


# DHCP

