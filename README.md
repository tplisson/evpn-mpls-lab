# EVPN-MPLS LAB
Ansible playbook repo for an EVPN-MPLS lab using Juniper MX routers (MX10003).

## Structure
Most of these Ansible playbooks use Jinja2 templates located under the `templates` directory.\
Global variables are defined under the `group_vars` directory.\
Host unique variables are defined within the `host_vars` directory.

## Requirements
Docker image for Juniper Ansible roles for Junos
```
docker pull juniper/pyez-ansible
docker run -it --rm -v $(pwd):/project juniper/pyez-ansible
```
Ansible Galaxy modules for Junos 
https://hub.docker.com/r/juniper/pyez-ansible/


## Lab Topology
Physical Topology
![Image1 of lab topology](https://github.com/tplisson/evpn-mpls-lab/blob/master/lab-topology-1.jpg)

EVPN Instances spread across DCs with traffic steered through SRX firewall
![Image2 of lab topology](https://github.com/tplisson/evpn-mpls-lab/blob/master/lab-topology-2.jpg)

Single EVPN instance spanned both DCs
![Image2 of lab topology](https://github.com/tplisson/evpn-mpls-lab/blob/master/lab-topology-3.jpg)

