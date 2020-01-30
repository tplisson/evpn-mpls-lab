# EVPN-MPLS LAB
Ansible playbook repo for an EVPN-MPLS lab

## Structure
Most of these Ansible playbooks use Jinja2 templates located under the 'templates' directory.
Global variables are defined under the 'group_vars' directory.
Host unique variables are defined within the 'host_vars' directory.

## Lab Topology
![Image of lab topology](https://github.com/tplisson/evpn-mpls-lab/lab-topology.png)

## Requirements
Docker image for Juniper Ansible roles for Junos
https://hub.docker.com/r/juniper/pyez-ansible/
