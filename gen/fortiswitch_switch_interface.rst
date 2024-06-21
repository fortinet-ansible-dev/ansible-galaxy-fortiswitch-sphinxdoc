:source: fortiswitch_switch_interface.py

:orphan:

.. fortiswitch_switch_interface:

fortiswitch_switch_interface -- Usable interfaces (trunks and ports) in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch feature and interface category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_interface</td>
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
    <li> <span class="li-head">switch_interface</span> - Usable interfaces (trunks and ports). <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">allow_arp_monitor</span> - Enable/Disable ARP monitoring. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">allowed_sub_vlans</span> - Sub-VLANs allowed to egress this interface. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">allowed_vlans</span> - Allowed VLANs. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">arp_inspection_trust</span> - Dynamic ARP Inspection (trusted or untrusted). <span class="li-normal">type: str</span> <span class="li-normal">choices: trusted, untrusted</span> </li>
        <li> <span class="li-head">auto_discovery_fortilink</span> - Enable/disable automatic FortiLink discovery mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">auto_discovery_fortilink_packet_interval</span> - FortiLink packet interval for automatic discovery (3 - 300 sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">default_cos</span> - Set default COS for untagged packets. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dhcp_snoop_learning_limit</span> - Maximum DHCP IP learned on the interface. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcp_snoop_learning_limit_check</span> - Enable/Disable DHCP learning limit check on the interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">dhcp_snoop_option82_override</span> - Configure per vlan option82 override. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">circuit_id</span> - Text String of Circuit Id. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - Vlan Id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">remote_id</span> - Text String of Remote Id. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">dhcp_snoop_option82_trust</span> - Enable/Disable (allow/disallow) dhcp pkt with option82 on untrusted interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">dhcp_snooping</span> - DHCP snooping interface (trusted or untrusted). <span class="li-normal">type: str</span> <span class="li-normal">choices: trusted, untrusted</span> </li>
        <li> <span class="li-head">discard_mode</span> - Configure discard mode for interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, all-tagged, all-untagged</span> </li>
        <li> <span class="li-head">edge_port</span> - Enable/disable interface as edge port. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">filter_sub_vlans</span> - Private VLAN or sub-VLAN based port type. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">fortilink_l3_mode</span> - FortiLink L3 uplink port. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">igmp_snooping_flood_reports</span> - Enable/disable flooding of IGMP snooping reports to this interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">interface_mode</span> - Set interface mode - L2 or L3. <span class="li-normal">type: str</span> <span class="li-normal">choices: L2, L3</span> </li>
        <li> <span class="li-head">ip_mac_binding</span> - Enable/disable ip-mac-binding on this interaface. <span class="li-normal">type: str</span> <span class="li-normal">choices: global, enable, disable</span> </li>
        <li> <span class="li-head">learning_limit</span> - Limit the number of dynamic MAC addresses on this port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">learning_limit_action</span> - Enable/disable turning off this interface on learn limit violation. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, shutdown</span> </li>
        <li> <span class="li-head">log_mac_event</span> - Enable/disable logging for dynamic MAC address events. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">loop_guard</span> - Enable/disable loop guard protection. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">loop_guard_mac_move_threshold</span> - Trigger loop guard if MAC move per second of this interface reaches this threshold. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">loop_guard_timeout</span> - Loop guard disabling protection (min). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mcast_snooping_flood_traffic</span> - Enable/disable flooding of multicast snooping traffic to this interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mld_snooping_flood_reports</span> - Enable/disable flooding of MLD reports to this interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">nac</span> - Enable/disable NAC in Fortilink mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">name</span> - Interface name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">native_vlan</span> - Native (untagged) VLAN. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">packet_sample_rate</span> - Packet sample rate (0 - 99999). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">packet_sampler</span> - Enable/disable packet sampling. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">port_security</span> - Configure port security. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">allow_mac_move</span> - Enable/disable allow mac move mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">allow_mac_move_to</span> - Enable/disable allow mac move mode to this port. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">auth_fail_vlan</span> - Enable/disable auth_fail vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">auth_fail_vlanid</span> - Set auth_fail vlanid. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">auth_order</span> - set authentication auth order. <span class="li-normal">type: str</span> <span class="li-normal">choices: dot1x-MAB, MAB-dot1x, MAB</span> </li>
            <li> <span class="li-head">auth_priority</span> - set authentication auth priority. <span class="li-normal">type: str</span> <span class="li-normal">choices: legacy, dot1x-MAB, MAB-dot1x</span> </li>
            <li> <span class="li-head">authserver_timeout_period</span> - Set authserver_timeout period. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">authserver_timeout_tagged</span> - Set authserver_timeout tagged vlan mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, lldp-voice, static</span> </li>
            <li> <span class="li-head">authserver_timeout_tagged_lldp_voice_vlanid</span> - authserver_timeout tagged lldp voice vlanid. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">authserver_timeout_tagged_vlanid</span> - Set authserver_timeout tagged vlanid. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">authserver_timeout_vlan</span> - Enable/disable authserver_timeout vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">authserver_timeout_vlanid</span> - Set authserver_timeout vlanid. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">dacl</span> - Enable/disable dynamic access control list mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">eap_auto_untagged_vlans</span> - Enable/disable EAP auto-untagged-vlans mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">eap_egress_tagged</span> - Enable/disable Egress frame tag. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">eap_passthru</span> - Enable/disable EAP pass-through mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">framevid_apply</span> - Enable/disable the capbility to apply the EAP/MAB frame vlan to the port native vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">guest_auth_delay</span> - Set guest auth delay. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">guest_vlan</span> - Enable/disable guest vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">guest_vlanid</span> - Set guest vlanid. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">mab_eapol_request</span> - Set MAB EAPOL Request. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">mac_auth_bypass</span> - Enable/disable mac-authentication-bypass on this interaface. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">macsec_pae_mode</span> - Assign PAE mode to a MACSEC interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, supp, auth</span> </li>
            <li> <span class="li-head">macsec_profile</span> - macsec port profile. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">open_auth</span> - Enable/disable open authentication on this interaface. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">port_security_mode</span> - Security mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, 802.1X, 802.1X-mac-based, macsec</span> </li>
            <li> <span class="li-head">quarantine_vlan</span> - Enable/disable Quarantine VLAN detection. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">radius_timeout_overwrite</span> - Enable/disable radius server session timeout to overwrite local timeout. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            </ul>
        <li> <span class="li-head">primary_vlan</span> - Private VLAN to host. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">private_vlan</span> - Configure private VLAN. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, promiscuous, sub-vlan</span> </li>
        <li> <span class="li-head">private_vlan_port_type</span> - Private VLAN or sub-VLAN based port type. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ptp_policy</span> - PTP policy. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ptp_status</span> - PTP Admin. Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">qnq</span> - Configure QinQ. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">add_inner</span> - Add inner-tag for untagged packets upon ingress. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">allowed_c_vlan</span> - Allowed c vlans. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">edge_type</span> - Choose edge type. <span class="li-normal">type: str</span> <span class="li-normal">choices: customer</span> </li>
            <li> <span class="li-head">native_c_vlan</span> - Native c vlan for untagged packets. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">priority</span> - Follow S-Tag or C-Tag"s priority. <span class="li-normal">type: str</span> <span class="li-normal">choices: follow-c-tag, follow-s-tag</span> </li>
            <li> <span class="li-head">remove_inner</span> - Remove inner-tag upon egress. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">s_tag_priority</span> - Set priority value if packets follow S-Tag"s priority. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">status</span> - Enable/Disable QinQ mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">stp_qnq_admin</span> - Enable/Disable QnQ to manage STP admin status. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">untagged_s_vlan</span> - Add s-vlan to untagged packet. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">vlan_mapping</span> - Configure Vlan Mapping. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">description</span> - Description of Mapping entry. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">id</span> - Entry Id. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">match_c_vlan</span> - Matching customer(inner) vlan. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">new_s_vlan</span> - Set new service vlan. <span class="li-normal">type: int</span> </li>
                </ul>
            <li> <span class="li-head">vlan_mapping_miss_drop</span> - Enabled or disabled drop if mapping missed. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            </ul>
        <li> <span class="li-head">qos_policy</span> - QOS egress COS queue policy. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">raguard</span> - IPV6 RA guard configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">raguard_policy</span> - RA Guard policy name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">vlan_list</span> - Vlan list. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">rpvst_port</span> - Enable/disable interface to inter-op with pvst <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">sample_direction</span> - SFlow sample direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: tx, rx, both</span> </li>
        <li> <span class="li-head">security_groups</span> - Group name. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Group name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">sflow_counter_interval</span> - SFlow sampler counter polling interval (0:disable - 255). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">snmp_index</span> - SNMP index. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">sticky_mac</span> - Enable/disable Sticky MAC for this interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">stp_bpdu_guard</span> - Enable/disable STP BPDU guard protection (stp-state and edge-port must be enabled). <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">stp_bpdu_guard_timeout</span> - BPDU Guard disabling protection (min). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">stp_loop_protection</span> - Enable/disable spanning tree protocol loop guard protection (stp-state must be enabled). <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">stp_root_guard</span> - Enable/disable STP root guard protection (stp-state must be enabled). <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">stp_state</span> - Enable/disable spanning tree protocol. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">sub_vlan</span> - Private VLAN sub-VLAN to host. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">switch_port_mode</span> - Enable/disable port as L2 switch port (enable) or as pure routed port (disable). <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">trust_dot1p_map</span> - QOS trust 802.1p map. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trust_ip_dscp_map</span> - QOS trust IP-DSCP map. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">type</span> - Interface type. <span class="li-normal">type: str</span> <span class="li-normal">choices: physical, trunk</span> </li>
        <li> <span class="li-head">untagged_vlans</span> - Configure VLANs permitted to be transmitted without VLAN tags. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">vlan_mapping</span> - Configure vlan mapping table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">action</span> - Vlan action if packet is matched. <span class="li-normal">type: str</span> <span class="li-normal">choices: add, replace, delete</span> </li>
            <li> <span class="li-head">description</span> - Description of Mapping entry. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">direction</span> - Ingress or Egress direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: ingress, egress</span> </li>
            <li> <span class="li-head">id</span> - Entry Id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">match_c_vlan</span> - Matching customer(inner) vlan. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">match_s_vlan</span> - Matching service(outer) vlan. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">new_s_vlan</span> - Set new service(outer) vlan. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">vlan_mapping_miss_drop</span> - Enabled or disabled drop if mapping missed. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">vlan_tpid</span> - Configure ether-type. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">vlan_traffic_type</span> - Configure traffic tagging. <span class="li-normal">type: str</span> <span class="li-normal">choices: untagged, tagged</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Usable interfaces (trunks and ports).
      fortinet.fortiswitch.fortiswitch_switch_interface:
          state: "present"
          switch_interface:
              allow_arp_monitor: "disable"
              allowed_sub_vlans: "<your_own_value>"
              allowed_vlans: "<your_own_value>"
              arp_inspection_trust: "trusted"
              auto_discovery_fortilink: "disable"
              auto_discovery_fortilink_packet_interval: "8"
              default_cos: "9"
              description: "<your_own_value>"
              dhcp_snoop_learning_limit: "11"
              dhcp_snoop_learning_limit_check: "disable"
              dhcp_snoop_option82_override:
                  -
                      circuit_id: "<your_own_value>"
                      id: "15 (source switch.vlan.id)"
                      remote_id: "<your_own_value>"
              dhcp_snoop_option82_trust: "enable"
              dhcp_snooping: "trusted"
              discard_mode: "none"
              edge_port: "enabled"
              filter_sub_vlans: "disable"
              fortilink_l3_mode: "enable"
              igmp_snooping_flood_reports: "enable"
              interface_mode: "L2"
              ip_mac_binding: "global"
              learning_limit: "26"
              learning_limit_action: "none"
              log_mac_event: "enable"
              loop_guard: "enabled"
              loop_guard_mac_move_threshold: "30"
              loop_guard_timeout: "31"
              mcast_snooping_flood_traffic: "enable"
              mld_snooping_flood_reports: "enable"
              nac: "enable"
              name: "default_name_35"
              native_vlan: "36"
              packet_sample_rate: "37"
              packet_sampler: "enabled"
              port_security:
                  allow_mac_move: "disable"
                  allow_mac_move_to: "disable"
                  auth_fail_vlan: "disable"
                  auth_fail_vlanid: "43"
                  auth_order: "dot1x-MAB"
                  auth_priority: "legacy"
                  authserver_timeout_period: "46"
                  authserver_timeout_tagged: "disable"
                  authserver_timeout_tagged_lldp_voice_vlanid: "48"
                  authserver_timeout_tagged_vlanid: "49"
                  authserver_timeout_vlan: "disable"
                  authserver_timeout_vlanid: "51"
                  dacl: "disable"
                  eap_auto_untagged_vlans: "disable"
                  eap_egress_tagged: "disable"
                  eap_passthru: "disable"
                  framevid_apply: "disable"
                  guest_auth_delay: "57"
                  guest_vlan: "disable"
                  guest_vlanid: "59"
                  mab_eapol_request: "60"
                  mac_auth_bypass: "disable"
                  macsec_pae_mode: "none"
                  macsec_profile: "<your_own_value> (source switch.macsec.profile.name)"
                  open_auth: "disable"
                  port_security_mode: "none"
                  quarantine_vlan: "disable"
                  radius_timeout_overwrite: "disable"
              primary_vlan: "68 (source switch.vlan.id)"
              private_vlan: "disable"
              private_vlan_port_type: "70"
              ptp_policy: "<your_own_value> (source switch.ptp.policy.name)"
              ptp_status: "enable"
              qnq:
                  add_inner: "74"
                  allowed_c_vlan: "<your_own_value>"
                  edge_type: "customer"
                  native_c_vlan: "77"
                  priority: "follow-c-tag"
                  remove_inner: "disable"
                  s_tag_priority: "80"
                  status: "disable"
                  stp_qnq_admin: "disable"
                  untagged_s_vlan: "83"
                  vlan_mapping:
                      -
                          description: "<your_own_value>"
                          id: "86"
                          match_c_vlan: "87"
                          new_s_vlan: "88"
                  vlan_mapping_miss_drop: "disable"
              qos_policy: "<your_own_value> (source switch.qos.qos-policy.name)"
              raguard:
                  -
                      id: "92"
                      raguard_policy: "<your_own_value> (source switch.raguard-policy.name)"
                      vlan_list: "<your_own_value>"
              rpvst_port: "enabled"
              sample_direction: "tx"
              security_groups:
                  -
                      name: "default_name_98"
              sflow_counter_interval: "99"
              snmp_index: "100"
              sticky_mac: "enable"
              stp_bpdu_guard: "enabled"
              stp_bpdu_guard_timeout: "103"
              stp_loop_protection: "enabled"
              stp_root_guard: "enabled"
              stp_state: "enabled"
              sub_vlan: "107 (source switch.vlan.id)"
              switch_port_mode: "disable"
              trust_dot1p_map: "<your_own_value> (source switch.qos.dot1p-map.name)"
              trust_ip_dscp_map: "<your_own_value> (source switch.qos.ip-dscp-map.name)"
              type: "physical"
              untagged_vlans: "<your_own_value>"
              vlan_mapping:
                  -
                      action: "add"
                      description: "<your_own_value>"
                      direction: "ingress"
                      id: "117"
                      match_c_vlan: "118"
                      match_s_vlan: "119"
                      new_s_vlan: "120"
              vlan_mapping_miss_drop: "disable"
              vlan_tpid: "<your_own_value> (source switch.vlan-tpid.name)"
              vlan_traffic_type: "untagged"


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
