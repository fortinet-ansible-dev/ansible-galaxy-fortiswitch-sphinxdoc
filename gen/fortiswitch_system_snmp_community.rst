:source: fortiswitch_system_snmp_community.py

:orphan:

.. fortiswitch_system_snmp_community:

fortiswitch_system_snmp_community -- SNMP community configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system_snmp feature and community category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_snmp_community</td>
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
    <li> <span class="li-head">system_snmp_community</span> - SNMP community configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">events</span> - Trap snmp events. <span class="li-normal">type: str</span> <span class="li-normal">choices: cpu-high, mem-low, log-full, intf-ip, ent-conf-change, llv, l2mac, sensor-fault, sensor-alarm, fan-detect, psu-status, ip-conflict, tkmem-hb-oo-sync, fsTrapStitch1, fsTrapStitch2, fsTrapStitch3, fsTrapStitch4, fsTrapStitch5, storm-control</span> </li>
        <li> <span class="li-head">hosts</span> - Allow hosts configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Host entry id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Allow interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ip</span> - Allow host ip address and netmask. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">source_ip</span> - Source ip for snmp trap. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">hosts6</span> - Allow hosts configuration for IPv6. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Host6 entry id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Allow interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ipv6</span> - Allow host ipv6 address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">source_ipv6</span> - Source ipv6 for snmp trap. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">id</span> - Community id. <span class="li-normal">type: int</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">name</span> - Community name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">query_v1_port</span> - SNMP v1 query port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">query_v1_status</span> - Enable/disable snmp v1 query. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">query_v2c_port</span> - SNMP v2c query port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">query_v2c_status</span> - Enable/disable snmp v2c query. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable this commuity. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">trap_v1_lport</span> - SNMP v1 trap local port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trap_v1_rport</span> - SNMP v1 trap remote port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trap_v1_status</span> - Enable/disable snmp v1 trap. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">trap_v2c_lport</span> - SNMP v2c trap local port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trap_v2c_rport</span> - SNMP v2c trap remote port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trap_v2c_status</span> - Enable/disable snmp v2c trap. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: SNMP community configuration.
      fortinet.fortiswitch.fortiswitch_system_snmp_community:
          state: "present"
          system_snmp_community:
              events: "cpu-high"
              hosts:
                  -
                      id: "5"
                      interface: "<your_own_value> (source system.interface.name)"
                      ip: "<your_own_value>"
                      source_ip: "<your_own_value>"
              hosts6:
                  -
                      id: "10"
                      interface: "<your_own_value> (source system.interface.name)"
                      ipv6: "<your_own_value>"
                      source_ipv6: "<your_own_value>"
              id: "14"
              name: "default_name_15"
              query_v1_port: "16"
              query_v1_status: "enable"
              query_v2c_port: "18"
              query_v2c_status: "enable"
              status: "enable"
              trap_v1_lport: "21"
              trap_v1_rport: "22"
              trap_v1_status: "enable"
              trap_v2c_lport: "24"
              trap_v2c_rport: "25"
              trap_v2c_status: "enable"


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
