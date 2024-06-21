:source: fortiswitch_switch_acl_802_1x.py

:orphan:

.. fortiswitch_switch_acl_802_1x:

fortiswitch_switch_acl_802_1x -- 802-1X Radius Dynamic Ingress Policy configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_acl feature and 802_1x category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_acl_802_1x</td>
 <td><code class="docutils literal notranslate">v7.0.2 -> 7.4.3 </code></td>
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
    <li> <span class="li-head">switch_acl_802_1x</span> - 802-1X Radius Dynamic Ingress Policy configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">access_list_entry</span> - Access Control List Entry configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">action</span> - Actions for the policy. <span class="li-normal">type: dict</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">count</span> - Count enable/disable action. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">drop</span> - Drop enable/disable action. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                </ul>
            <li> <span class="li-head">classifier</span> - Match-conditions for the policy. <span class="li-normal">type: dict</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">dst_ip_prefix</span> - Destination-ip address to be matched. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">dst_mac</span> - Destination mac address to be matched. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">ether_type</span> - Ether type to be matched. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">service</span> - Service name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">src_ip_prefix</span> - Source-ip address to be matched. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">src_mac</span> - Source mac address to be matched. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">vlan_id</span> - Vlan id to be matched. <span class="li-normal">type: int</span> </li>
                </ul>
            <li> <span class="li-head">description</span> - Description of the policy. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">group</span> - Group ID of the policy. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">id</span> - Ingress policy ID. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">description</span> - Description of the policy. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">filter_id</span> - filter-id of the policy. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">id</span> - 802-1X Dynamic Ingress policy ID. <span class="li-normal">type: int</span> <span class="li-required">required: true</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: 802-1X Radius Dynamic Ingress Policy configuration.
      fortinet.fortiswitch.fortiswitch_switch_acl_802_1x:
          state: "present"
          switch_acl_802_1x:
              access_list_entry:
                  -
                      action:
                          count: "enable"
                          drop: "enable"
                      classifier:
                          dst_ip_prefix: "<your_own_value>"
                          dst_mac: "<your_own_value>"
                          ether_type: "10"
                          service: "<your_own_value> (source switch.acl.service.custom.name)"
                          src_ip_prefix: "<your_own_value>"
                          src_mac: "<your_own_value>"
                          vlan_id: "14"
                      description: "<your_own_value>"
                      group: "16"
                      id: "17"
              description: "<your_own_value>"
              filter_id: "<your_own_value>"
              id: "20"


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
