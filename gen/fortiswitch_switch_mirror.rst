:source: fortiswitch_switch_mirror.py

:orphan:

.. fortiswitch_switch_mirror:

fortiswitch_switch_mirror -- Packet mirror in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch feature and mirror category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_mirror</td>
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
    <li> <span class="li-head">switch_mirror</span> - Packet mirror. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">dst</span> - Destination interface. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">encap_gre_protocol</span> - Protocol value in the ERSPAN GRE header. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">encap_ipv4_src</span> - IPv4 source address in the ERSPAN IP header. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">encap_ipv4_tos</span> - TOS, or DSCP and ECN, values in the ERSPAN IP header. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">encap_ipv4_ttl</span> - IPv4 time-to-live value in the ERSPAN IP header. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">encap_mac_dst</span> - Nexthop/Gateway MAC address on the path to the ERSPAN collector IP. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">encap_mac_src</span> - Source MAC address in the ERSPAN ethernet header. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">encap_vlan</span> - Control the tagged/untagged status of ERSPAN encapsulation headers. <span class="li-normal">type: str</span> <span class="li-normal">choices: tagged, untagged</span> </li>
        <li> <span class="li-head">encap_vlan_cfi</span> - CFI or DEI bit in the ERSPAN or RSPAN VLAN header. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">encap_vlan_id</span> - VLAN ID in the ERSPAN or RSPAN VLAN header. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">encap_vlan_priority</span> - Priority code point value in the ERSPAN or RSPAN VLAN header. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">encap_vlan_tpid</span> - TPID in the ERSPAN or RSPAN VLAN header. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">erspan_collector_ip</span> - ERSPAN collector IP address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">mode</span> - Mirroring mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: SPAN, RSPAN, ERSPAN-manual, ERSPAN-auto, RSPAN-manual, RSPAN-auto</span> </li>
        <li> <span class="li-head">name</span> - Mirror session name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">rspan_ip</span> - RSPAN destination IP address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">src_egress</span> - Source egress interfaces. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">src_ingress</span> - Source ingress interfaces. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: active, inactive</span> </li>
        <li> <span class="li-head">strip_mirrored_traffic_tags</span> - Enable/disable stripping of VLAN tags from mirrored traffic. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">switching_packet</span> - Enable/disable switching functionality when mirroring. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Packet mirror.
      fortinet.fortiswitch.fortiswitch_switch_mirror:
          state: "present"
          switch_mirror:
              dst: "<your_own_value> (source switch.interface.name)"
              encap_gre_protocol: "4"
              encap_ipv4_src: "<your_own_value>"
              encap_ipv4_tos: "6"
              encap_ipv4_ttl: "127"
              encap_mac_dst: "<your_own_value>"
              encap_mac_src: "<your_own_value>"
              encap_vlan: "tagged"
              encap_vlan_cfi: "0"
              encap_vlan_id: "2047"
              encap_vlan_priority: "3"
              encap_vlan_tpid: "14"
              erspan_collector_ip: "<your_own_value>"
              mode: "SPAN"
              name: "default_name_17"
              rspan_ip: "<your_own_value>"
              src_egress:
                  -
                      name: "default_name_20 (source switch.physical-port.name)"
              src_ingress:
                  -
                      name: "default_name_22 (source switch.physical-port.name)"
              status: "active"
              strip_mirrored_traffic_tags: "enable"
              switching_packet: "enable"


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
