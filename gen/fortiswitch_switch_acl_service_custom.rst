:source: fortiswitch_switch_acl_service_custom.py

:orphan:

.. fortiswitch_switch_acl_service_custom:

fortiswitch_switch_acl_service_custom -- Custom service configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_acl_service feature and custom category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_acl_service_custom</td>
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
    <li> <span class="li-head">switch_acl_service_custom</span> - Custom service configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">color</span> - Set GUI icon color. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">comment</span> - Comments. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">icmpcode</span> - ICMP code. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">icmptype</span> - ICMP type. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">name</span> - Custom service name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">protocol</span> - Protocol type. <span class="li-normal">type: str</span> <span class="li-normal">choices: TCP/UDP/SCTP, ICMP, IP</span> </li>
        <li> <span class="li-head">protocol_number</span> - IP protocol number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">sctp_portrange</span> - Multiple sctp port ranges. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">tcp_portrange</span> - Multiple tcp port ranges. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">udp_portrange</span> - Multiple udp port ranges. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Custom service configuration.
      fortinet.fortiswitch.fortiswitch_switch_acl_service_custom:
          state: "present"
          switch_acl_service_custom:
              color: "3"
              comment: "Comments."
              icmpcode: "5"
              icmptype: "6"
              name: "default_name_7"
              protocol: "TCP/UDP/SCTP"
              protocol_number: "9"
              sctp_portrange: "<your_own_value>"
              tcp_portrange: "<your_own_value>"
              udp_portrange: "<your_own_value>"


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
