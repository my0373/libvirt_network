libvirt_network
=========

A simple role to configure KVM virtual networks.



Requirements
------------

Ansible 2.5+

Role Variables
--------------



#### libvirt_networks
A list of networks to be configured. Networks are defined as YAML dictionaries. Currently only NAT networks are supported. 

#### libvirt_net_name
The name of the network to be configured

#### libvirt_net_gateway
The gateway address toconfigure

#### libvirt_net_subnet
The subnet address to configure

#### libvirt_dhcp_start_address
If libvirt_enable_dhcp is set, then configure this to be the start of the DHCP range.

#### libvirt_dhcp_end_address
If libvirt_enable_dhcp is set, then configure this to be the end of the DHCP range.

#### libvirt_enable_dhcp
When set, the network will be configured to use DHCP.
Possibel options are True or False.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: hypervisor
      roles:
        ## Configure the libvirt networks
        - libvirt_network

License
-------

MIT

Author Information
------------------
Matt York
my0373@gmail.com
