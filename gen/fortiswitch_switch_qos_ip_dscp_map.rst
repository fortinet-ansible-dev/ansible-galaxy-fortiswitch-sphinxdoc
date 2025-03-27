:source: fortiswitch_switch_qos_ip_dscp_map.py

:orphan:

.. fortiswitch_switch_qos_ip_dscp_map:

fortiswitch_switch_qos_ip_dscp_map -- QOS IP precedence/DSCP configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_qos feature and ip_dscp_map category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_qos_ip_dscp_map</td>
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
    <li> <span class="li-head">switch_qos_ip_dscp_map</span> - QOS IP precedence/DSCP configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">description</span> - Description of the map name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">map</span> - Maps between IP-DSCP value to COS queue. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">cos_queue</span> - COS queue number. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">diffserv</span> - Differentiated service. <span class="li-normal">type: str</span> <span class="li-normal">choices: CS0, CS1, AF11, AF12, AF13, CS2, AF21, AF22, AF23, CS3, AF31, AF32, AF33, CS4, AF41, AF42, AF43, CS5, EF, CS6, CS7</span> </li>
            <li> <span class="li-head">entry_name</span> - Mapping entry. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ip_precedence</span> - IP precedence. <span class="li-normal">type: str</span> <span class="li-normal">choices: Network-Control, Internetwork-Control, Critic/ECP, FlashOverride, Flash, Immediate, Priority, Routine</span> </li>
            <li> <span class="li-head">type</span> - type <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">value</span> - Raw values of DSCP (0 - 63). <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">name</span> - DSCP map name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: QOS IP precedence/DSCP configuration.
      fortinet.fortiswitch.fortiswitch_switch_qos_ip_dscp_map:
          state: "present"
          switch_qos_ip_dscp_map:
              description: "<your_own_value>"
              map:
                  -
                      cos_queue: "3"
                      diffserv: "CS0"
                      entry_name: "<your_own_value>"
                      ip_precedence: "Network-Control"
                      type: "9"
                      value: "<your_own_value>"
              name: "default_name_11"


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
