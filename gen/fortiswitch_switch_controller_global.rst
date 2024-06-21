:source: fortiswitch_switch_controller_global.py

:orphan:

.. fortiswitch_switch_controller_global:

fortiswitch_switch_controller_global -- Switch-controller global configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_controller feature and global category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_controller_global</td>
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
    <li> <span class="li-head">switch_controller_global</span> - Switch-controller global configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">ac_data_port</span> - Switch controller data port [1024, 49150]. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ac_dhcp_option_code</span> - DHCP option code for CAPUTP AC. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ac_discovery_mc_addr</span> - Discovery multicast address <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ac_discovery_type</span> - AC discovery type. <span class="li-normal">type: str</span> <span class="li-normal">choices: static, dhcp, broadcast, multicast, auto, disable</span> </li>
        <li> <span class="li-head">ac_list</span> - AC list. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ipv4_address</span> - IP addr. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ipv6_address</span> - IPv6 address. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">ac_port</span> - Switch controller ctl port [1024, 49150]. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">echo_interval</span> - Interval before SWTP sends Echo Request after joining AC. [1, 600] default = 30s. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">location</span> - Location. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">max_discoveries</span> - The maximum <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">max_retransmit</span> - The maximum <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mgmt_mode</span> - FortiLink management mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: capwap, https</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">tunnel_mode</span> - Compatible/strict tunnel mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: compatible, strict</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Switch-controller global configuration.
      fortinet.fortiswitch.fortiswitch_switch_controller_global:
          switch_controller_global:
              ac_data_port: "3"
              ac_dhcp_option_code: "4"
              ac_discovery_mc_addr: "<your_own_value>"
              ac_discovery_type: "static"
              ac_list:
                  -
                      id: "8"
                      ipv4_address: "<your_own_value>"
                      ipv6_address: "<your_own_value>"
              ac_port: "11"
              echo_interval: "12"
              location: "<your_own_value>"
              max_discoveries: "14"
              max_retransmit: "15"
              mgmt_mode: "capwap"
              name: "default_name_17"
              tunnel_mode: "compatible"


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
