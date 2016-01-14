midonet-agent
=============

Ansible role for midolman, the MidoNet Agent
This is the Openvswitch datapath controller and must run in all the Hypervisor hosts.

Requirements
------------

Ubuntu or RedHat/CentOS

Role Variables
--------------

* Required:

`zookeeper_hosts` should be a dictionary or group in hosts inventory with all zookeeper members.
`midonet_password` is the administration password needed for midonet API.

* Not Required:

`agent_template` is one of the agent predefined profiles, agent-compute-medium by default:

agent-compute-large
agent-compute-medium
agent-gateway-large
agent-gateway-medium
default

If `tz_name` is defined, host will be added to the specified tunnel zone.

The rest of midonet variables should be configured in midonet-cluster role.

Dependencies
------------

Midonet repositories ( abelboldu.midonet-repos )


Example Playbook
----------------

```
- hosts: zookeeper
    roles:
      - role: abelboldu.midonet-agent
        zookeeper_hosts: '{{ groups["zookeeper"] }}'
        midonet_password: 'midonet'
```



License
-------

Apache 2.0

Author Information
------------------