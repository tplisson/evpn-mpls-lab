# EVPN-MPLS LAB
Ansible playbook repo for an EVPN-MPLS lab using Juniper MX routers (MX10003).

## Structure
Most of these Ansible playbooks use Jinja2 templates located under the `templates` directory.\
Global variables are defined under the `group_vars` directory.\
Host unique variables are defined within the `host_vars` directory.


## Lab Topology
![Image of lab topology](https://github.com/tplisson/evpn-mpls-lab/blob/master/lab-topology.png)

## Requirements
Docker image for Juniper Ansible roles for Junos
```
docker pull juniper/pyez-ansible
docker run -it --rm -v $(pwd):/project juniper/pyez-ansible
```
Ansible Galaxy modules for Junos 
https://hub.docker.com/r/juniper/pyez-ansible/