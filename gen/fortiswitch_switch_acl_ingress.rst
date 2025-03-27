:source: fortiswitch_switch_acl_ingress.py

:orphan:

.. fortiswitch_switch_acl_ingress:

fortiswitch_switch_acl_ingress -- Ingress Policy configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_acl feature and ingress category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_acl_ingress</td>
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
    <li> <span class="li-head">switch_acl_ingress</span> - Ingress Policy configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">action</span> - Actions for the policy. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">cos_queue</span> - COS queue number (0 - 7), or unset to disable. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">count</span> - Count enable/disable action. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">count_type</span> - Count-type(two colors): all, green, yellow, or red. <span class="li-normal">type: str</span> <span class="li-normal">choices: all, green, yellow, red</span> </li>
            <li> <span class="li-head">cpu_cos_queue</span> - CPU COS queue number(17 - 25). Only if packets reach to CPU. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">drop</span> - Drop enable/disable action. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">egress_mask</span> - List of physical ports to be configured in egress mask. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">member_name</span> - Physical port name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">mirror</span> - Mirror session name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">outer_vlan_tag</span> - Outer vlan tag. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">policer</span> - Policer id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">redirect</span> - Redirect interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">redirect_bcast_cpu</span> - Redirect broadcast to all ports including CPU. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">redirect_bcast_no_cpu</span> - Redirect broadcast to all ports excluding CPU. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">redirect_physical_port</span> - List of physical ports to redirect. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">member_name</span> - Physical port name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">remark_cos</span> - Remark CoS value (0 - 7), or unset to disable. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">remark_dscp</span> - Remark DSCP value (0 - 63), or unset to disable. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">classifier</span> - Match-conditions for the policy. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">cos</span> - 802.1Q CoS value to be matched. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">dscp</span> - DSCP value to be matched. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">dst_ip6_prefix</span> - Destination-ip6 address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">dst_ip_prefix</span> - Destination-ip address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">dst_mac</span> - Destination mac address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ether_type</span> - Ether type to be matched. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">l3_interface</span> - l3 interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">service</span> - Service name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">src_ip6_prefix</span> - Source-ip6 address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">src_ip_prefix</span> - Source-ip address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">src_mac</span> - Source mac address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">vlan_id</span> - Vlan id to be matched. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">description</span> - Description of the policy. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">group</span> - Group ID of the policy. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">id</span> - Ingress policy ID. <span class="li-normal">type: int</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">ingress_interface</span> - Interface list to which policy is bound on the ingress. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">member_name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">ingress_interface_all</span> - Select all interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">schedule</span> - schedule list. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">schedule_name</span> - Schedule name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">status</span> - Set policy status. <span class="li-normal">type: str</span> <span class="li-normal">choices: active, inactive</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Ingress Policy configuration.
      fortinet.fortiswitch.fortiswitch_switch_acl_ingress:
          state: "present"
          switch_acl_ingress:
              action:
                  cos_queue: "3"
                  count: "enable"
                  count_type: "all"
                  cpu_cos_queue: "12"
                  drop: "enable"
                  egress_mask:
                      -
                          member_name: "<your_own_value> (source switch.physical-port.name)"
                  mirror: "<your_own_value> (source switch.mirror.name)"
                  outer_vlan_tag: "2047"
                  policer: "13 (source switch.acl.policer.id)"
                  redirect: "<your_own_value> (source switch.physical-port.name switch.trunk.name)"
                  redirect_bcast_cpu: "enable"
                  redirect_bcast_no_cpu: "enable"
                  redirect_physical_port:
                      -
                          member_name: "<your_own_value> (source switch.physical-port.name)"
                  remark_cos: "3"
                  remark_dscp: "31"
              classifier:
                  cos: "3"
                  dscp: "31"
                  dst_ip6_prefix: "<your_own_value>"
                  dst_ip_prefix: "<your_own_value>"
                  dst_mac: "<your_own_value>"
                  ether_type: "32767"
                  l3_interface: "<your_own_value> (source system.interface.name)"
                  service: "<your_own_value> (source switch.acl.service.custom.name)"
                  src_ip6_prefix: "<your_own_value>"
                  src_ip_prefix: "<your_own_value>"
                  src_mac: "<your_own_value>"
                  vlan_id: "2047"
              description: "<your_own_value>"
              group: "35"
              id: "36"
              ingress_interface:
                  -
                      member_name: "<your_own_value> (source switch.physical-port.name switch.trunk.name)"
              ingress_interface_all: "enable"
              schedule:
                  -
                      schedule_name: "<your_own_value> (source system.schedule.onetime.name system.schedule.recurring.name system.schedule.group.name)"
              status: "active"


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
