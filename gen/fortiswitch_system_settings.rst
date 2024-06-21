:source: fortiswitch_system_settings.py

:orphan:

.. fortiswitch_system_settings:

fortiswitch_system_settings -- Settings in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and settings category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_settings</td>
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
    <li> <span class="li-head">system_settings</span> - Settings. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">allow_subnet_overlap</span> - Allow one interface subnet overlap with other interfaces. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">asymroute</span> - Asymmetric route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">asymroute6</span> - Asymmetric route6. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bfd</span> - Enable Bidirectional Forwarding Detection (BFD) on all interfaces. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bfd_desired_min_tx</span> - BFD desired minimal tx interval. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bfd_detect_mult</span> - BFD detection multiplier. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bfd_dont_enforce_src_port</span> - Verify Source Port of BFD Packets. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bfd_required_min_rx</span> - BFD required minimal rx interval. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">comments</span> - Vd comments. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">device</span> - Interface. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ecmp_max_paths</span> - Maximum number of ECMP next-hops. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">gateway</span> - Default gateway ip address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip</span> - IP address and netmask. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip_ecmp_mode</span> - IP ecmp mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: source-ip-based, dst-ip-based, port-based</span> </li>
        <li> <span class="li-head">manageip</span> - IP address and netmask. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">multicast_forward</span> - Multicast forwarding. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">multicast_skip_policy</span> - Skip policy check, and allow multicast through. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">multicast_ttl_notchange</span> - Multicast ttl not change. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">opmode</span> - Firewall operation mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: nat</span> </li>
        <li> <span class="li-head">per_ip_bandwidth</span> - Per-ip-bandwidth disable. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">sccp_port</span> - TCP port the SCCP proxy will monitor for SCCP traffic. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">sip_helper</span> - Helper to add dynamic sip firewall allow rule. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">sip_nat_trace</span> - Add original IP if NATed. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">sip_tcp_port</span> - TCP port the SIP proxy will monitor for SIP traffic. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">sip_udp_port</span> - UDP port the SIP proxy will monitor for SIP traffic. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable this VDOM. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">strict_src_check</span> - Strict source verification. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">utf8_spam_tagging</span> - Convert spam tags to UTF8 for better non-ascii character support. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">vpn_stats_log</span> - Enable periodic VPN log statistics. <span class="li-normal">type: str</span> <span class="li-normal">choices: ipsec, pptp, l2tp, ssl</span> </li>
        <li> <span class="li-head">vpn_stats_period</span> - Period to send VPN log statistics (seconds). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">wccp_cache_engine</span> - Enable wccp cache engine or not. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Settings.
      fortinet.fortiswitch.fortiswitch_system_settings:
          system_settings:
              allow_subnet_overlap: "enable"
              asymroute: "enable"
              asymroute6: "enable"
              bfd: "enable"
              bfd_desired_min_tx: "7"
              bfd_detect_mult: "8"
              bfd_dont_enforce_src_port: "enable"
              bfd_required_min_rx: "10"
              comments: "<your_own_value>"
              device: "<your_own_value> (source system.interface.name)"
              ecmp_max_paths: "13"
              gateway: "<your_own_value>"
              ip: "<your_own_value>"
              ip_ecmp_mode: "source-ip-based"
              manageip: "<your_own_value>"
              multicast_forward: "enable"
              multicast_skip_policy: "enable"
              multicast_ttl_notchange: "enable"
              opmode: "nat"
              per_ip_bandwidth: "disable"
              sccp_port: "23"
              sip_helper: "enable"
              sip_nat_trace: "enable"
              sip_tcp_port: "26"
              sip_udp_port: "27"
              status: "enable"
              strict_src_check: "enable"
              utf8_spam_tagging: "enable"
              vpn_stats_log: "ipsec"
              vpn_stats_period: "32"
              wccp_cache_engine: "enable"


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
