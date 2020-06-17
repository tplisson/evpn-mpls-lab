[![Build Status](https://travis-ci.org/tplisson/evpn-mpls-lab.svg?branch=master)](https://travis-ci.org/tplisson/evpn-mpls-lab)

# EVPN-MPLS LAB
Ansible playbook repository for an EVPN-MPLS lab using Juniper MX routers (MX10003).

## Structure
All Ansible playbooks are located under the `playbooks` directory.\
Most of these Ansible playbooks use Jinja2 templates located under the `templates` directory.\
Global variables are defined under the `group_vars` directory.\
Host unique variables are defined within the `host_vars` directory.

## Requirements
Docker image for Juniper Ansible roles for Junos
```
docker pull juniper/pyez-ansible
docker run -it --rm -v $(pwd):/playbooks juniper/pyez-ansible
```
Ansible Galaxy modules for Junos version 2.3.0\
https://hub.docker.com/r/juniper/pyez-ansible/

This repository has been tested using:\
Ansible 2.9.5\
Ansible Galaxy "Juniper.junos" role  version 2.4.1


## Lab Topology
Physical Topology
![Image1 of lab topology](https://github.com/tplisson/evpn-mpls-lab/blob/master/lab-topology-1.jpg)

EVPN Instances spread across DCs with traffic steered through SRX firewall
![Image2 of lab topology](https://github.com/tplisson/evpn-mpls-lab/blob/master/lab-topology-2.jpg)

Single EVPN instance spanned both DCs
![Image2 of lab topology](https://github.com/tplisson/evpn-mpls-lab/blob/master/lab-topology-3.jpg)

## Lab Testing
List of tests

Index	| Test Name
--- | --- 
**0** | **0.BASELINE**
**1**	| **Steady State**
1-1	| 1-1-STEADY-ISIS-SPRING
1-2	| 1-2-STEADY-TI-LFA
1-3	| 1-3-STEADY-BGP
1-4	| 1-4-STEADY-EVI30-L3VPN
1-5	| 1-5-STEADY-EVI30-TYPE5
1-6	| 1-6-STEADY-EVI10-20-SRX-L3VPN
1-7	| 1-7-STEADY-EVI10-20-SRX-TYPE5
**2**	| **EVI 30 L3VPN Convergence Tests**
2-1	| 	2-1-LF-CONVERG-EVI30-L3VPN
2-2	| 	2-2-NF-CONVERG-EVI30-L3VPN
**3** |	**EVI 30 Type5 Convergence Tests**
3-1	| 	3-1-LF-CONVERG-EVI30-TYPE5
3-2	| 	3-3-NF-CONVERG-EVI30-TYPE5
**4** |	**EVIs 10+20 L3VPN Convergence Tests**
4-1	| 	4-1-LF-CONVERG-EVI10-20-SRX-L3VPN
4-2	| 	4-2-NF-CONVERG-EVI10-20-SRX-L3VPN
**5** |	**EVIs 10+20 Type5 Convergence Tests**
5-1	| 	5-1-LF-CONVERG-EVI10-20-SRX-T5
**6** |	**Multicast Testing**
6-1	| 	6-1-MCAST-IGMP
6-2	| 	6-2-MCAST-MLD
**7** |	**SRX RG Failover Testing**
7-1 |   7-1-RG-FAILOVER-EVI10-20-SRX-L3VPN
7-2 |   7-2-RG-FAILOVER-EVI10-20-SRX-TYPE5
