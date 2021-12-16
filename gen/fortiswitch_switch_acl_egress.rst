:source: fortiswitch_switch_acl_egress.py

:orphan:

.. fortiswitch_switch_acl_egress:

fortiswitch_switch_acl_egress -- Egress Policy configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.11

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_acl feature and egress category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 </tr>
 <tr>
 <td>fortiswitch_switch_acl_egress</td>
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
    <li> <span class="li-head">switch_acl_egress</span> - Egress Policy configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">action</span> - Actions for the policy. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">count</span> - Count enable/disable action. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">drop</span> - Drop enable/disable action. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">mirror</span> - Mirror session name. Source switch.mirror.name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">outer_vlan_tag</span> - Outer vlan tag. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">policer</span> - Policer id. Source switch.acl.policer.id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">redirect</span> - Redirect interface name. Source switch.physical-port.name switch.trunk.name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">remark_dscp</span> - Remark DSCP value (0 - 63), or unset to disable. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">classifier</span> - Match-conditions for the policy. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">cos</span> - 802.1Q CoS value to be matched. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">dscp</span> - DSCP value to be matched. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">dst_ip_prefix</span> - Destination-ip address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">dst_mac</span> - Destination mac address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ether_type</span> - Ether type to be matched. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">service</span> - Service name. Source switch.acl.service.custom.name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">src_ip_prefix</span> - Source-ip address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">src_mac</span> - Source mac address to be matched. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">vlan_id</span> - Vlan id to be matched. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">description</span> - Description of the policy. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">group</span> - Group ID of the policy. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">id</span> - Egress policy ID. <span class="li-normal">type: int</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">interface</span> - Interface to which policy is bound on the egress. Source switch.physical-port.name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">schedule</span> - schedule list. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">schedule_name</span> - Schedule name. Source system.schedule.onetime.name system.schedule.recurring.name system.schedule.group.name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">status</span> - Set policy status. <span class="li-normal">type: str</span> <span class="li-normal">choices: active, inactive</span> </li>
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
      - name: Egress Policy configuration.
        fortiswitch_switch_acl_egress:
          state: "present"
          switch_acl_egress:
            action:
                count: "enable"
                drop: "enable"
                mirror: "<your_own_value> (source switch.mirror.name)"
                outer_vlan_tag: "7"
                policer: "8 (source switch.acl.policer.id)"
                redirect: "<your_own_value> (source switch.physical-port.name switch.trunk.name)"
                remark_dscp: "10"
            classifier:
                cos: "12"
                dscp: "13"
                dst_ip_prefix: "<your_own_value>"
                dst_mac: "<your_own_value>"
                ether_type: "16"
                service: "<your_own_value> (source switch.acl.service.custom.name)"
                src_ip_prefix: "<your_own_value>"
                src_mac: "<your_own_value>"
                vlan_id: "20"
            description: "<your_own_value>"
            group: "22"
            id:  "23"
            interface: "<your_own_value> (source switch.physical-port.name)"
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
- Nicolas Thomas (@thomnico)


.. hint::
    If you notice any issues in this documentation, you can create a pull request to improve it.
