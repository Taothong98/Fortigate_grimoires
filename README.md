﻿
-  1. [This is topology for test in  lab,](#Thisistopologyfortestinlab)
-  2. [Interface](#Interface)
-  3. [step 1 Interface  Role](#step1InterfaceRole)
-  4. [step 2 SD-WAN Zones](#step2SD-WANZones)
-  5. [step 3 Performance SLAs](#step3PerformanceSLAs)
-  6. [step 4  SD-WAN Rules](#step4SD-WANRules)


# SD-WAN
####  1. <a name='Thisistopologyfortestinlab'></a>This is topology for test in  lab,, 
 
![topology](image-sdwan/typology.png)
  - the section sd-wan we are just foucus firewall 1 
   
####  2. <a name='Interface'></a>Interface

![interfacewan](image-sdwan/interfacewan.png)
- make sure whether interface wan both 2 can connect to the internet.

##  <a name='step1InterfaceRole'></a>step 0.5 Interface  Role

![rolewan1.png](image-sdwan/rolewan1.png)
![rolewan2.png](image-sdwan/rolewan2.png)
![shorolewan.png](image-sdwan/shorolewan.png)


##  <a name='step2SD-WANZones'></a>step 1 SD-WAN Zones

![click-virtualwanlink.png](image-sdwan/click-virtualwanlink.png)

![interfacemember.png](image-sdwan/interfacemember.png)


![create-int-wan1.png](image-sdwan/create-int-wan1.png)
![create-int-wan2.png](image-sdwan/create-int-wan2.png)

![addintface-invirtual-wan-link.png](image-sdwan/addintface-invirtual-wan-link.png)

![after-add-int.png](image-sdwan/after-add-int.png)

##  <a name='step3PerformanceSLAs'></a>step 2 Performance SLAs
#### This step is for creating performance measures, which we use for comparative performance between WAN1 and WAN2.


![create-sla.png](image-sdwan/create-sla.png)

![setting-sla.png](image-sdwan/setting-sla.png)

-It success
![sh-after-set-sla.png](image-sdwan/sh-after-set-sla.png)


##  <a name='step4SD-WANRules'></a>step 3  SD-WAN Rules
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

