:source: fortiswitch_switch_vlan.py

:orphan:

.. fortiswitch_switch_vlan:

fortiswitch_switch_vlan -- Configure optional per-VLAN settings in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch feature and vlan category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



Requirements
------------
The below requirements are needed on the host that executes this module.

- ansible>=2.11


FortiSW Version Compatibility
-----------------------------


.. raw:: html

 <br>
 <table>
 <tr>
 <td></td>
 <td><code class="docutils literal notranslate">v7.0.0 </code></td>
 <td><code class="docutils literal notranslate">v7.0.1 </code></td>
 <td><code class="docutils literal notranslate">v7.0.2 </code></td>
 <td><code class="docutils literal notranslate">v7.0.3 </code></td>
 </tr>
 <tr>
 <td>fortiswitch_switch_vlan</td>
 <td>yes</td>
 <td>yes</td>
 <td>yes</td>
 <td>yes</td>
 </tr>
 </table>
 <p>



Parameters
----------


.. raw:: html

    <ul>
    <li> <span class="li-head">enable_log</span> - Enable/Disable logging for task. <span class="li-normal">type: bool</span> <span class="li-required">required: false</span> <span class="li-normal">default: False</span> </li>
    <li> <span class="li-head">member_path</span> - Member attribute path to operate on. <span class="li-normal">type: str</span> </li>
    <li> <span class="li-head">member_state</span> - Add or delete a member under specified attribute path. <span class="li-normal">type: str</span> <span class="li-normal">choices: present, absent</span> </li>
    <li> <span class="li-head">state</span> - Indicates whether to create or remove the object. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> <span class="li-normal">choices: present, absent</span> </li>
    <li> <span class="li-head">switch_vlan</span> - Configure optional per-VLAN settings. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">access_vlan</span> - Block port-to-port traffic. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">arp_inspection</span> - Enable/Disable Dynamic ARP Inspection. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">community_vlans</span> - Communities within this private VLAN. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">cos_queue</span> - Set cos(0-7) on the VLAN traffic or unset to disable. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dhcp_server_access_list</span> - Configure dhcp server access list. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - User given name for dhcp-server. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">server_ip</span> - IP address for DHCP Server. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">server_ip6</span> - IP address for DHCPv6 Server. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">dhcp_snooping</span> - Enable/Disable dhcp snooping on this vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">dhcp_snooping_option82</span> - Enable/Disable inserting option82. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">dhcp_snooping_verify_mac</span> - Enable/Disable verify source mac. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">dhcp6_snooping</span> - Enable/Disable DHCPv6 snooping on this vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">id</span> - VLAN ID. <span class="li-normal">type: int</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">igmp_snooping</span> - Enable/disable IGMP-snooping for the VLAN interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">igmp_snooping_fast_leave</span> - Enable/disable IGMP snooping fast leave. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">igmp_snooping_proxy</span> - Enable/disable IGMP snooping proxy for the VLAN interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">igmp_snooping_querier</span> - Enable/disable IGMP-snooping-querier for the VLAN interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">igmp_snooping_querier_addr</span> - IGMP-snooping-querier address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">igmp_snooping_querier_version</span> - IGMP-snooping-querier version. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">igmp_snooping_static_group</span> - IGMP static groups. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">mcast_addr</span> - Multicast address for static-group. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">members</span> - Member interfaces. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">member_name</span> - Interface name. Source switch.interface.name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">name</span> - Group name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">isolated_vlan</span> - Isolated VLAN. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lan_segment</span> - Enable/disable LAN Segment. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">lan_segment_primary_vlan</span> - LAN Segment Primary VLAN ID. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lan_segment_type</span> - LAN segment type. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lan_subvlans</span> - LAN segment subvlans. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">learning</span> - Enable/disable L2 learning on this VLAN. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">learning_limit</span> - Limit the number of dynamic MAC addresses on this VLAN. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">member_by_ipv4</span> - Assign VLAN membership based on IPv4 address or subnet. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">address</span> - Address(/32) or subnet. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - Entry ID. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">member_by_ipv6</span> - Assign VLAN membership based on IPv6 prefix. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - Entry ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix</span> - IPv6 prefix (max = /64). <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">member_by_mac</span> - Assign VLAN membership based on MAC address. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - Entry ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">mac</span> - MAC address. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">member_by_proto</span> - Assign VLAN membership based on ethernet frametype and protocol. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">frametypes</span> - Ethernet frame types to check. <span class="li-normal">type: str</span> <span class="li-normal">choices: ethernet2, 802.3d, llc</span> </li>
            <li> <span class="li-head">id</span> - Entry ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">protocol</span> - Ethernet protocols (0 - 65535). <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">mld_snooping</span> - Enable/disable MLD snooping for the VLAN interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mld_snooping_fast_leave</span> - Enable/disable MLD snooping fast leave. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mld_snooping_proxy</span> - Enable/disable MLD snooping proxy for the VLAN interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mld_snooping_querier</span> - Enable/disable MLD snooping querier for the VLAN interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mld_snooping_querier_addr</span> - MLD-querier address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">mld_snooping_static_group</span> - MLD static groups. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">mcast_addr</span> - IPv6 Multicast address for static-group. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">members</span> - Member interfaces. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">member_name</span> - Interface name. Source switch.interface.name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">name</span> - Group name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">mrouter_ports</span> - Member interfaces. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">member_name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">policer</span> - Set policer on the VLAN traffic. Source switch.acl.policer.id. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">primary_vlan</span> - Primary VLAN ID. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">private_vlan</span> - Enable/disable private VLAN. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">private_vlan_type</span> - Private VLAN type. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">rspan_mode</span> - Stop L2 learning and interception of BPDUs and other packets on this VLAN. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - hosts: fortiswitch01
      collections:
        - fortinet.fortiswitch
      connection: httpapi
      vars:
       ansible_httpapi_use_ssl: yes
       ansible_httpapi_validate_certs: no
       ansible_httpapi_port: 443
      tasks:
      - name: Configure optional per-VLAN settings.
        fortiswitch_switch_vlan:
          state: "present"
          switch_vlan:
            access_vlan: "disable"
            arp_inspection: "disable"
            community_vlans: "<your_own_value>"
            cos_queue: "6"
            description: "<your_own_value>"
            dhcp_server_access_list:
             -
                name: "default_name_9"
                server_ip: "<your_own_value>"
                server_ip6: "<your_own_value>"
            dhcp_snooping: "disable"
            dhcp_snooping_option82: "disable"
            dhcp_snooping_verify_mac: "disable"
            dhcp6_snooping: "disable"
            id:  "16"
            igmp_snooping: "enable"
            igmp_snooping_fast_leave: "enable"
            igmp_snooping_proxy: "enable"
            igmp_snooping_querier: "enable"
            igmp_snooping_querier_addr: "<your_own_value>"
            igmp_snooping_querier_version: "22"
            igmp_snooping_static_group:
             -
                mcast_addr: "<your_own_value>"
                members:
                 -
                    member_name: "<your_own_value> (source switch.interface.name)"
                name: "default_name_27"
            isolated_vlan: "28"
            lan_segment: "enable"
            lan_segment_primary_vlan: "30"
            lan_segment_type: "31"
            lan_subvlans: "<your_own_value>"
            learning: "disable"
            learning_limit: "34"
            member_by_ipv4:
             -
                address: "<your_own_value>"
                description: "<your_own_value>"
                id:  "38"
            member_by_ipv6:
             -
                description: "<your_own_value>"
                id:  "41"
                prefix: "<your_own_value>"
            member_by_mac:
             -
                description: "<your_own_value>"
                id:  "45"
                mac: "<your_own_value>"
            member_by_proto:
             -
                description: "<your_own_value>"
                frametypes: "ethernet2"
                id:  "50"
                protocol: "51"
            mld_snooping: "enable"
            mld_snooping_fast_leave: "enable"
            mld_snooping_proxy: "enable"
            mld_snooping_querier: "enable"
            mld_snooping_querier_addr: "<your_own_value>"
            mld_snooping_static_group:
             -
                mcast_addr: "<your_own_value>"
                members:
                 -
                    member_name: "<your_own_value> (source switch.interface.name)"
                name: "default_name_61"
            mrouter_ports:
             -
                member_name: "<your_own_value>"
            policer: "64 (source switch.acl.policer.id)"
            primary_vlan: "65"
            private_vlan: "enable"
            private_vlan_type: "67"
            rspan_mode: "enable"
    


Return Values
-------------
Common return values are documented: https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#common-return-values, the following are the fields unique to this module:

.. raw:: html

    <ul>

    <li> <span class="li-return">build</span> - Build number of the fortiSwitch image <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 1547</span></li>
    <li> <span class="li-return">http_method</span> - Last method used to provision the content into FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: PUT</span></li>
    <li> <span class="li-return">http_status</span> - Last result given by FortiSwitch on last operation applied <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 200</span></li>
    <li> <span class="li-return">mkey</span> - Master key (id) used in the last call to FortiSwitch <span class="li-normal">returned: success</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: id</span></li>
    <li> <span class="li-return">name</span> - Name of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: urlfilter</span></li>
    <li> <span class="li-return">path</span> - Path of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: webfilter</span></li>
    <li> <span class="li-return">serial</span> - Serial number of the unit <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: FS1D243Z13000122</span></li>
    <li> <span class="li-return">status</span> - Indication of the operation's result <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: success</span></li>
    <li> <span class="li-return">version</span> - Version of the FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: v7.0.0</span></li>
    </ul>

Status
------

- This module is not guaranteed to have a backwards compatible interface.


Authors
-------

- Link Zheng (@chillancezen)
- Jie Xue (@JieX19)
- Hongbin Lu (@fgtdev-hblu)
- Frank Shen (@frankshen01)
- Miguel Angel Munoz (@mamunozgonzalez)


.. hint::
    If you notice any issues in this documentation, you can create a pull request to improve it.
