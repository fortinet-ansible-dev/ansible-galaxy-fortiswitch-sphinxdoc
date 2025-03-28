:source: fortiswitch_switch_trunk.py

:orphan:

.. fortiswitch_switch_trunk:

fortiswitch_switch_trunk -- Link-aggregation in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch feature and trunk category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_trunk</td>
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
    <li> <span class="li-head">switch_trunk</span> - Link-aggregation. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">aggregator_mode</span> - LACP Member Select Mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: bandwidth, count</span> </li>
        <li> <span class="li-head">auto_isl</span> - Trunk with auto-isl. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bundle</span> - Enable bundle. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">fallback_port</span> - LACP fallback port. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">fortilink</span> - FortiLink trunk. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">hb_dst_ip</span> - Destination IP address of heartbeat packet. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">hb_dst_udp_port</span> - Destination UDP port of heartbeat packet. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">hb_in_vlan</span> - Receive VLAN ID in heartbeat packet. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">hb_out_vlan</span> - Transmit VLAN ID in heartbeat packet. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">hb_src_ip</span> - Source IP address of heartbeat packet. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">hb_src_udp_port</span> - Source UDP port of heartbeat packet. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">hb_verify</span> - Enable/disable heartbeat packet strict validation. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">isl_fortilink</span> - ISL fortiLink trunk. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lacp_speed</span> - LACP speed. <span class="li-normal">type: str</span> <span class="li-normal">choices: slow, fast</span> </li>
        <li> <span class="li-head">max_bundle</span> - Maximum size of bundle. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">max_miss_heartbeats</span> - Maximum tolerant missed heartbeats. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mclag</span> - Multi Chassis LAG. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mclag_icl</span> - MCLAG inter-chassis-link. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mclag_mac_address</span> - MCLAG MAC address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">member_withdrawal_behavior</span> - Port behaviors after it withdraws because of loss of control packets. <span class="li-normal">type: str</span> <span class="li-normal">choices: forward, block</span> </li>
        <li> <span class="li-head">members</span> - Aggregated interfaces. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">member_name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">min_bundle</span> - Minimum size of bundle. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mode</span> - Link Aggreation mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: static, lacp-passive, lacp-active, fortinet-trunk</span> </li>
        <li> <span class="li-head">name</span> - Trunk name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">port_extension</span> - Port extension enable. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">port_extension_trigger</span> - Number of failed port to trigger the whole trunk down. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">port_selection_criteria</span> - Algorithm for aggregate port selection. <span class="li-normal">type: str</span> <span class="li-normal">choices: src-mac, dst-mac, src-dst-mac, src-ip, dst-ip, src-dst-ip</span> </li>
        <li> <span class="li-head">restricted</span> - Restricted ISL ICL trunk. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">static_isl</span> - Static ISL. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">static_isl_auto_vlan</span> - User ISL auto VLAN. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">trunk_id</span> - Internal id. <span class="li-normal">type: int</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Link-aggregation.
      fortinet.fortiswitch.fortiswitch_switch_trunk:
          state: "present"
          switch_trunk:
              aggregator_mode: "bandwidth"
              auto_isl: "4"
              bundle: "enable"
              description: "<your_own_value>"
              fallback_port: "<your_own_value>"
              fortilink: "8"
              hb_dst_ip: "<your_own_value>"
              hb_dst_udp_port: "10"
              hb_in_vlan: "11"
              hb_out_vlan: "12"
              hb_src_ip: "<your_own_value>"
              hb_src_udp_port: "14"
              hb_verify: "enable"
              isl_fortilink: "16"
              lacp_speed: "slow"
              max_bundle: "18"
              max_miss_heartbeats: "19"
              mclag: "enable"
              mclag_icl: "enable"
              mclag_mac_address: "<your_own_value>"
              member_withdrawal_behavior: "forward"
              members:
                  -
                      member_name: "<your_own_value> (source switch.physical-port.name)"
              min_bundle: "26"
              mode: "static"
              name: "default_name_28"
              port_extension: "enable"
              port_extension_trigger: "30"
              port_selection_criteria: "src-mac"
              restricted: "0"
              static_isl: "enable"
              static_isl_auto_vlan: "enable"
              trunk_id: "35"


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
