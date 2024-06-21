:source: fortiswitch_system_interface.py

:orphan:

.. fortiswitch_system_interface:

fortiswitch_system_interface -- Configure interfaces in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and interface category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



Requirements
------------
The below requirements are needed on the host that executes this module.

- ansible>=2.15


FortiSwitch Version Compatibility
---------------------------------


.. raw:: html

 <br>
 <table border="1">
 <tr>
 <td></td><td colspan="1">Supported Version Ranges</td>
 </tr>
 <tr>
 <td>fortiswitch_system_interface</td>
 <td><code class="docutils literal notranslate">v7.0.0 -> 7.4.3 </code></td>
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
    <li> <span class="li-head">system_interface</span> - Configure interfaces. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">alias</span> - Alias. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">allowaccess</span> - Interface management access. <span class="li-normal">type: list</span> <span class="li-normal">choices: ping, https, http, ssh, snmp, telnet, radius-acct</span> </li>
        <li> <span class="li-head">auth_type</span> - PPP authentication type. <span class="li-normal">type: str</span> <span class="li-normal">choices: auto, pap, chap, mschapv1, mschapv2</span> </li>
        <li> <span class="li-head">bfd</span> - Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: global, enable, disable</span> </li>
        <li> <span class="li-head">bfd_desired_min_tx</span> - BFD desired minimal transmit interval. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bfd_detect_mult</span> - BFD detection multiplier. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bfd_required_min_rx</span> - BFD required minimal receive interval. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">cli_conn_status</span> - CLI connection status. <span class="li-normal">type: str</span> <span class="li-normal">choices: initial, connecting, connected, failed</span> </li>
        <li> <span class="li-head">defaultgw</span> - Enable/disable default gateway. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">detectprotocol</span> - Protocol to use for gateway detection. <span class="li-normal">type: str</span> <span class="li-normal">choices: ping, tcp-echo, udp-echo</span> </li>
        <li> <span class="li-head">detectserver</span> - IP address to PING for gateway detection. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dhcp_client_identifier</span> - DHCP client identifier. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dhcp_client_status</span> - DHCP client connection status. <span class="li-normal">type: str</span> <span class="li-normal">choices: initial, stopped, connected, rebooting, selecting, requesting, binding, renewing, rebinding</span> </li>
        <li> <span class="li-head">dhcp_expire</span> - DHCP client expiration. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcp_relay_ip</span> - DHCP relay IP address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dhcp_relay_option82</span> - Enable / Disable DHCP relay option-82 insertion. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">dhcp_relay_service</span> - Enable/disable use DHCP relay service. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">dhcp_vendor_specific_option</span> - DHCP Vendor specific option 43. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">distance</span> - Distance of learned routes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dns_server_override</span> - Enable/disable use of DNS server aquired by DHCP or PPPoE. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">dynamic_dns1</span> - Primary dynamic DNS server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dynamic_dns2</span> - Secondary dynamic DNS server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dynamicgw</span> - Dynamic gateway. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">forward_domain</span> - TP mode forward domain. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">gwdetect</span> - Enable/disable gateway detection. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">ha_priority</span> - PING server HA election priority (1 - 50). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">icmp_redirect</span> - Enable/disable ICMP rediect. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">interface</span> - Interface name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip</span> - Interface IPv4 address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ipv6</span> - IPv6 address. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">autoconf</span> - Enable/disable address automatic config. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">dhcp6_information_request</span> - Enable/disable DHCPv6 information request. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ip6_address</span> - Primary IPv6 address prefix of interface. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ip6_allowaccess</span> - Allow management access to the interface. <span class="li-normal">type: list</span> <span class="li-normal">choices: any, ping, https, http, ssh, snmp, telnet, radius-acct</span> </li>
            <li> <span class="li-head">ip6_default_life</span> - IPv6 default life (sec). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip6_dns_server_override</span> - Enable/disable using the DNS server acquired by DHCP. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ip6_extra_addr</span> - Extra IPv6 address prefixes of interface. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">prefix</span> - IPv6 address prefix. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">ip6_hop_limit</span> - IPv6 hop limit. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip6_link_mtu</span> - IPv6 link MTU. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip6_manage_flag</span> - Enable/disable sending of IPv6 managed flag. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ip6_max_interval</span> - IPv6 maximum interval (sec) after which RA will be sent. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip6_min_interval</span> - IPv6 minimum interval (sec) after which RA will be sent. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip6_mode</span> - Addressing mode (static, DHCP). <span class="li-normal">type: str</span> <span class="li-normal">choices: static, dhcp</span> </li>
            <li> <span class="li-head">ip6_other_flag</span> - Enable/disable sending of IPv6 other flag. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ip6_prefix_list</span> - IPv6 advertised prefix list. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">autonomous_flag</span> - Enable/disable autonomous flag. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">onlink_flag</span> - Enable/disable onlink flag. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">preferred_life_time</span> - Preferred life time (sec). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">prefix</span> - IPv6 prefix. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">valid_life_time</span> - Valid life time (sec). <span class="li-normal">type: int</span> </li>
                </ul>
            <li> <span class="li-head">ip6_reachable_time</span> - IPv6 reachable time (milliseconds). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip6_retrans_time</span> - IPv6 retransmit time (milliseconds). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip6_send_adv</span> - Enable/disable sending of IPv6 Router advertisement. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ip6_unknown_mcast_to_cpu</span> - Enable/disable unknown mcast to cpu. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">vrip6_link_local</span> - Link-local IPv6 address of virtual router. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">vrrp6</span> - IPv6 VRRP configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">accept_mode</span> - Enable/disable accept mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">adv_interval</span> - Advertisement interval (1 - 255 seconds). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">preempt</span> - Enable/disable preempt mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">priority</span> - Priority of the virtual router (1 - 255). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">start_time</span> - Startup time (1 - 255 seconds). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">status</span> - Enable/disable VRRP. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">vrdst6</span> - Monitor the route to this destination. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">vrgrp</span> - VRRP group ID (1 - 65535). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">vrid</span> - Virtual router identifier (1 - 255). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">vrip6</span> - IPv6 address of the virtual router. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">vrrp_virtual_mac6</span> - Enable/disable virtual MAC for VRRP. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">l2_interface</span> - L2 interface name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">macaddr</span> - MAC address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">mode</span> - Interface addressing mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: static, dhcp</span> </li>
        <li> <span class="li-head">mtu</span> - Maximum transportation unit (MTU). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mtu_override</span> - Enable/disable override of default MTU. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">ping_serv_status</span> - PING server status. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">priority</span> - Priority of learned routes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">remote_ip</span> - Remote IP address of tunnel. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">secondary_IP</span> - Enable/disable use of secondary IP address. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">secondaryip</span> - Second IP address of interface. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">allowaccess</span> - Interface management access. <span class="li-normal">type: list</span> <span class="li-normal">choices: ping, https, http, ssh, snmp, telnet, radius-acct</span> </li>
            <li> <span class="li-head">detectprotocol</span> - Protocol to use for gateway detection. <span class="li-normal">type: str</span> <span class="li-normal">choices: ping, tcp-echo, udp-echo</span> </li>
            <li> <span class="li-head">detectserver</span> - IP address to PING for gateway detection. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">gwdetect</span> - Enable/disable gateway detection. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ha_priority</span> - PING server HA election priority (1 - 50). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">id</span> - Id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip</span> - Interface IPv4 address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ping_serv_status</span> - PING server status. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">snmp_index</span> - SNMP index. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">speed</span> - Speed (copper mode port only). <span class="li-normal">type: str</span> <span class="li-normal">choices: auto, 10full, 10half, 100full, 100half, 1000full, 1000half, 1000auto</span> </li>
        <li> <span class="li-head">src_check</span> - Enable/disable source IP check. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, loose, strict</span> </li>
        <li> <span class="li-head">src_check_allow_default</span> - Enable/disable.When src ip lookup hits default route,enable means allow pkt else drop. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">status</span> - Interface status. <span class="li-normal">type: str</span> <span class="li-normal">choices: up, down</span> </li>
        <li> <span class="li-head">switch</span> - Contained in switch. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">switch_members</span> - Switch interfaces. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">member_name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">type</span> - Interface type. <span class="li-normal">type: str</span> <span class="li-normal">choices: physical, vlan, tunnel, loopback, switch, hard-switch, vap-switch, hdlc, vxlan</span> </li>
        <li> <span class="li-head">vdom</span> - Virtual domain name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">vlanforward</span> - Enable/disable VLAN forwarding. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">vlanid</span> - VLAN ID. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">vrf</span> - VRF. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">vrrp</span> - VRRP configuration <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">adv_interval</span> - Advertisement interval (1 - 255 seconds). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">backup_vmac_fwd</span> - Enable/disable backup-vmac-fwd. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">preempt</span> - Enable/disable preempt mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">priority</span> - Priority of the virtual router (1 - 255). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">start_time</span> - Startup time (1 - 255 seconds). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">status</span> - Enable/disable status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">version</span> - VRRP version. <span class="li-normal">type: str</span> <span class="li-normal">choices: 2, 3</span> </li>
            <li> <span class="li-head">vrdst</span> - Monitor the route to this destination. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">vrgrp</span> - VRRP group ID (1 - 65535). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">vrid</span> - Virtual router identifier (1 - 255). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">vrip</span> - IP address of the virtual router. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">vrrp_virtual_mac</span> - enable to use virtual MAC for VRRP <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">weight</span> - Default weight for static routes if route has no weight configured (0 - 255). <span class="li-normal">type: int</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja

    - name: Configure interfaces.
      fortinet.fortiswitch.fortiswitch_system_interface:
          state: "present"
          system_interface:
              alias: "<your_own_value>"
              allowaccess: "ping"
              auth_type: "auto"
              bfd: "global"
              bfd_desired_min_tx: "7"
              bfd_detect_mult: "8"
              bfd_required_min_rx: "9"
              cli_conn_status: "initial"
              defaultgw: "enable"
              description: "<your_own_value>"
              detectprotocol: "ping"
              detectserver: "<your_own_value>"
              dhcp_client_identifier: "myId_15"
              dhcp_client_status: "initial"
              dhcp_expire: "17"
              dhcp_relay_ip: "<your_own_value>"
              dhcp_relay_option82: "disable"
              dhcp_relay_service: "disable"
              dhcp_vendor_specific_option: "<your_own_value>"
              distance: "22"
              dns_server_override: "enable"
              dynamic_dns1: "<your_own_value>"
              dynamic_dns2: "<your_own_value>"
              dynamicgw: "<your_own_value>"
              forward_domain: "27"
              gwdetect: "enable"
              ha_priority: "29"
              icmp_redirect: "enable"
              interface: "<your_own_value> (source system.interface.name)"
              ip: "<your_own_value>"
              ipv6:
                  autoconf: "enable"
                  dhcp6_information_request: "enable"
                  ip6_address: "<your_own_value>"
                  ip6_allowaccess: "any"
                  ip6_default_life: "38"
                  ip6_dns_server_override: "enable"
                  ip6_extra_addr:
                      -
                          prefix: "<your_own_value>"
                  ip6_hop_limit: "42"
                  ip6_link_mtu: "43"
                  ip6_manage_flag: "enable"
                  ip6_max_interval: "45"
                  ip6_min_interval: "46"
                  ip6_mode: "static"
                  ip6_other_flag: "enable"
                  ip6_prefix_list:
                      -
                          autonomous_flag: "enable"
                          onlink_flag: "enable"
                          preferred_life_time: "52"
                          prefix: "<your_own_value>"
                          valid_life_time: "54"
                  ip6_reachable_time: "55"
                  ip6_retrans_time: "56"
                  ip6_send_adv: "enable"
                  ip6_unknown_mcast_to_cpu: "enable"
                  vrip6_link_local: "<your_own_value>"
                  vrrp6:
                      -
                          accept_mode: "enable"
                          adv_interval: "62"
                          preempt: "enable"
                          priority: "64"
                          start_time: "65"
                          status: "enable"
                          vrdst6: "<your_own_value>"
                          vrgrp: "68"
                          vrid: "69"
                          vrip6: "<your_own_value>"
                  vrrp_virtual_mac6: "enable"
              l2_interface: "<your_own_value> (source switch.interface.name)"
              macaddr: "<your_own_value>"
              mode: "static"
              mtu: "75"
              mtu_override: "enable"
              name: "default_name_77"
              ping_serv_status: "78"
              priority: "79"
              remote_ip: "<your_own_value>"
              secondary_IP: "enable"
              secondaryip:
                  -
                      allowaccess: "ping"
                      detectprotocol: "ping"
                      detectserver: "<your_own_value>"
                      gwdetect: "enable"
                      ha_priority: "87"
                      id: "88"
                      ip: "<your_own_value>"
                      ping_serv_status: "90"
              snmp_index: "91"
              speed: "auto"
              src_check: "disable"
              src_check_allow_default: "enable"
              status: "up"
              switch: "<your_own_value>"
              switch_members:
                  -
                      member_name: "<your_own_value> (source switch.interface.name)"
              type: "physical"
              vdom: "<your_own_value> (source system.vdom.name)"
              vlanforward: "enable"
              vlanid: "102"
              vrf: "<your_own_value> (source router.vrf.name)"
              vrrp:
                  -
                      adv_interval: "105"
                      backup_vmac_fwd: "enable"
                      preempt: "enable"
                      priority: "108"
                      start_time: "109"
                      status: "enable"
                      version: "2"
                      vrdst: "<your_own_value>"
                      vrgrp: "113"
                      vrid: "114"
                      vrip: "<your_own_value>"
              vrrp_virtual_mac: "enable"
              weight: "117"


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
    If you notice any issues in this documentation, feel free to create a pull request to improve it.
