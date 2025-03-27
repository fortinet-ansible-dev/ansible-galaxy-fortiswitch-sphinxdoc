:source: fortiswitch_switch_global.py

:orphan:

.. fortiswitch_switch_global:

fortiswitch_switch_global -- Configure global settings in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch feature and global category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_global</td>
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
    <li> <span class="li-head">switch_global</span> - Configure global settings. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">access_vlan_mode</span> - Intra VLAN traffic behavior with loss of connection to the FortiGate. <span class="li-normal">type: str</span> <span class="li-normal">choices: legacy, fail-open, fail-close</span> </li>
        <li> <span class="li-head">auto_fortilink_discovery</span> - Enable/disable automatic FortiLink discovery. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">auto_isl</span> - Enable/Disable automatic inter switch LAG. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">auto_isl_port_group</span> - Configure global automatic inter-switch link port groups (overrides port level port groups). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">auto_stp_priority</span> - Automatic assignment of STP priority for tier1 and tier2 switches. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bpdu_learn</span> - Enable/disable BPDU learn. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">dhcp_snooping_database_export</span> - Enable/disable DHCP snoop database export to file. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">dmi_global_all</span> - Enable/disable DMI global status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">flapguard_retain_trigger</span> - Enable/disable retention of triggered state upon reboot. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">flood_unknown_multicast</span> - Enable/disable unknown mcast flood in the vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">flood_vtp</span> - Enable/disable Cisco VTP flood in the vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">forti_trunk_dmac</span> - Destination MAC address to be used for FortiTrunk heartbeat packets. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">fortilink_heartbeat_timeout</span> - Max fortilinkd echo replies that can be missed before fortilink is considered down. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">fortilink_p2p_native_vlan</span> - FortiLink point to point native VLAN. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">fortilink_p2p_tpid</span> - FortiLink point-to-point TPID. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">fortilink_vlan_optimization</span> - Controls VLAN assignment on ISL ports (assigns all 4k vlans when disabled). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">ip_mac_binding</span> - Configure ip-mac-binding status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">l2_memory_check</span> - Enable/disable L2 memory check, default interval is 120 seconds. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">l2_memory_check_interval</span> - User defined interval to check L2 memory(second). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">log_mac_limit_violations</span> - Enable/disable logs for Learning Limit Violations globally. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">loop_guard_tx_interval</span> - Loop guard packet Tx interval (sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mac_address</span> - Manually configured MAC address when mac-address-algorithm is set to manual. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mac_address_algorithm</span> - Method to configure the fifth byte of the MAC address <span class="li-normal">type: str</span> <span class="li-normal">choices: auto, manual</span> </li>
        <li> <span class="li-head">mac_aging_interval</span> - MAC address aging interval (sec; remove any MAC addresses unused since the the last check. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mac_violation_timer</span> - Set a global timeout for Learning Limit Violations (0 = disabled). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">max_path_in_ecmp_group</span> - Set max path in one ecmp group. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mclag_igmpsnooping_aware</span> - MCLAG IGMP-snooping aware. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mclag_peer_info_timeout</span> - MCLAG peer info timeout. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mclag_port_base</span> - MCLAG port base. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mclag_split_brain_all_ports_down</span> - Enable/disable MCLAG split brain all ports down <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">mclag_split_brain_detect</span> - Enable/disable MCLAG split brain detect. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mclag_split_brain_priority</span> - Set MCLAG split brain priority <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mclag_stp_aware</span> - MCLAG STP aware. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mirror_qos</span> - QOS value for locally mirrored traffic. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">poe_alarm_threshold</span> - Threshold (% of total power budget) above which an alarm event is generated. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">poe_guard_band</span> - Reserves power (W) in case of a spike in PoE consumption. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">poe_power_budget</span> - Set/override maximum power budget. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">poe_power_mode</span> - Set poe power mode to priority based or first come first served. <span class="li-normal">type: str</span> <span class="li-normal">choices: priority, first-come-first-served</span> </li>
        <li> <span class="li-head">poe_pre_standard_detect</span> - set poe-pre-standard-detect <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">port_security</span> - Global parameters for port-security. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">link_down_auth</span> - If link down detected, "set-unauth" reverts to un-authorized state. <span class="li-normal">type: str</span> <span class="li-normal">choices: set-unauth, no-action</span> </li>
            <li> <span class="li-head">mab_entry_as</span> - Confgure MAB MAC entry as static or dynamic. <span class="li-normal">type: str</span> <span class="li-normal">choices: static, dynamic</span> </li>
            <li> <span class="li-head">mab_reauth</span> - Enable or disable MAB reauthentication settings. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">mac_called_station_delimiter</span> - MAC called station delimiter . <span class="li-normal">type: str</span> <span class="li-normal">choices: hyphen, single-hyphen, colon, none</span> </li>
            <li> <span class="li-head">mac_calling_station_delimiter</span> - MAC calling station delimiter . <span class="li-normal">type: str</span> <span class="li-normal">choices: hyphen, single-hyphen, colon, none</span> </li>
            <li> <span class="li-head">mac_case</span> - MAC case . <span class="li-normal">type: str</span> <span class="li-normal">choices: uppercase, lowercase</span> </li>
            <li> <span class="li-head">mac_password_delimiter</span> - MAC authentication password delimiter . <span class="li-normal">type: str</span> <span class="li-normal">choices: hyphen, single-hyphen, colon, none</span> </li>
            <li> <span class="li-head">mac_username_delimiter</span> - MAC authentication username delimiter . <span class="li-normal">type: str</span> <span class="li-normal">choices: hyphen, single-hyphen, colon, none</span> </li>
            <li> <span class="li-head">max_reauth_attempt</span> - 802.1X/MAB maximum reauthorization attempt. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">quarantine_vlan</span> - Enable or disable Quarantine VLAN detection. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">reauth_period</span> - 802.1X/MAB reauthentication period ( minute ). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">tx_period</span> - 802.1X tx period ( second ). <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">storm_control_high_rate</span> - Storm control high rate. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">storm_control_monitor</span> - Enable/disable storm control monitor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">storm_control_rate_filter</span> - Storm control rate filter. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trunk_hash_mode</span> - Trunk hash mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: default, enhanced</span> </li>
        <li> <span class="li-head">trunk_hash_unicast_src_port</span> - Enable/disable source port in Unicast trunk hashing. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">trunk_hash_unkunicast_src_dst</span> - Enable/disable trunk hash for unknown unicast src-dst. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">virtual_wire_tpid</span> - TPID value used by virtual-wires. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">vlan_pruning</span> - Enable/disable VLAN pruning. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">vxlan_dport</span> - VXLAN destination UDP port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">vxlan_port</span> - VXLAN destination UDP port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">vxlan_sport</span> - VXLAN source UDP port (0 - 65535). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">vxlan_stp_virtual_mac</span> - Virtual STP root MAC address <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">vxlan_stp_virtual_root</span> - Enable/disable automatically making local switch the STP root for STP instances containing configured VXLAN"s access vlan. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Configure global settings.
      fortinet.fortiswitch.fortiswitch_switch_global:
          switch_global:
              access_vlan_mode: "legacy"
              auto_fortilink_discovery: "enable"
              auto_isl: "enable"
              auto_isl_port_group: "6"
              auto_stp_priority: "enable"
              bpdu_learn: "enable"
              dhcp_snooping_database_export: "enable"
              dmi_global_all: "enable"
              flapguard_retain_trigger: "enable"
              flood_unknown_multicast: "enable"
              flood_vtp: "enable"
              forti_trunk_dmac: "<your_own_value>"
              fortilink_heartbeat_timeout: "15"
              fortilink_p2p_native_vlan: "16"
              fortilink_p2p_tpid: "17"
              fortilink_vlan_optimization: "enable"
              ip_mac_binding: "enable"
              l2_memory_check: "enable"
              l2_memory_check_interval: "21"
              log_mac_limit_violations: "enable"
              loop_guard_tx_interval: "23"
              mac_address: "24"
              mac_address_algorithm: "auto"
              mac_aging_interval: "26"
              mac_violation_timer: "27"
              max_path_in_ecmp_group: "28"
              mclag_igmpsnooping_aware: "enable"
              mclag_peer_info_timeout: "30"
              mclag_port_base: "31"
              mclag_split_brain_all_ports_down: "disable"
              mclag_split_brain_detect: "enable"
              mclag_split_brain_priority: "34"
              mclag_stp_aware: "enable"
              mirror_qos: "36"
              name: "default_name_37"
              poe_alarm_threshold: "38"
              poe_guard_band: "39"
              poe_power_budget: "40"
              poe_power_mode: "priority"
              poe_pre_standard_detect: "enable"
              port_security:
                  link_down_auth: "set-unauth"
                  mab_entry_as: "static"
                  mab_reauth: "disable"
                  mac_called_station_delimiter: "hyphen"
                  mac_calling_station_delimiter: "hyphen"
                  mac_case: "uppercase"
                  mac_password_delimiter: "hyphen"
                  mac_username_delimiter: "hyphen"
                  max_reauth_attempt: "52"
                  quarantine_vlan: "disable"
                  reauth_period: "54"
                  tx_period: "55"
              storm_control_high_rate: "56"
              storm_control_monitor: "enable"
              storm_control_rate_filter: "58"
              trunk_hash_mode: "default"
              trunk_hash_unicast_src_port: "enable"
              trunk_hash_unkunicast_src_dst: "enable"
              virtual_wire_tpid: "62"
              vlan_pruning: "enable"
              vxlan_dport: "64"
              vxlan_port: "65"
              vxlan_sport: "32767"
              vxlan_stp_virtual_mac: "<your_own_value>"
              vxlan_stp_virtual_root: "enable"


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
