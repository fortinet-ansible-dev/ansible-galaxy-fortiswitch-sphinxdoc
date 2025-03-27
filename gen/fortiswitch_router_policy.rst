:source: fortiswitch_router_policy.py

:orphan:

.. fortiswitch_router_policy:

fortiswitch_router_policy -- Policy routing configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and policy category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_policy</td>
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
    <li> <span class="li-head">router_policy</span> - Policy routing configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">comments</span> - Description/comments. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dst</span> - Destination ip and mask. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">end_port</span> - End port number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">gateway</span> - IP address of gateway. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">input_device</span> - Incoming interface name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">interface</span> - Interface configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Interface name <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">pbr_map_name</span> - PBR policy map name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">nexthop_group</span> - Nexthop group (ECMP) configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">nexthop</span> - Nexthop configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">id</span> - Id (1-64). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">nexthop_ip</span> - IP address of nexthop. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">nexthop_vrf_name</span> - VRF name. <span class="li-normal">type: str</span> </li>
                </ul>
            </ul>
        <li> <span class="li-head">output_device</span> - Outgoing interface name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">pbr_map</span> - PBR map configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">comments</span> - Description/comments. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">rule</span> - Rule. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">dst</span> - Destination ip and mask. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">nexthop_group_name</span> - Nexthop group name. Used for ECMP. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">nexthop_ip</span> - IP address of nexthop. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">nexthop_vrf_name</span> - Nexthop vrf name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">seq_num</span> - Rule seq-num (1-10000). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">src</span> - Source ip and mask. <span class="li-normal">type: str</span> </li>
                </ul>
            </ul>
        <li> <span class="li-head">protocol</span> - Protocol number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">seq_num</span> - Sequence number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">src</span> - Source ip and mask. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">start_port</span> - Start port number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">tos</span> - Terms of service bit pattern. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">tos_mask</span> - Terms of service evaluated bits. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Policy routing configuration.
      fortinet.fortiswitch.fortiswitch_router_policy:
          state: "present"
          router_policy:
              comments: "<your_own_value>"
              dst: "<your_own_value>"
              end_port: "32767"
              gateway: "<your_own_value>"
              input_device: "<your_own_value> (source system.interface.name)"
              interface:
                  -
                      name: "default_name_9 (source system.interface.name)"
                      pbr_map_name: "<your_own_value>"
              nexthop_group:
                  -
                      name: "default_name_12"
                      nexthop:
                          -
                              id: "14"
                              nexthop_ip: "<your_own_value>"
                              nexthop_vrf_name: "<your_own_value> (source router.vrf.name)"
              output_device: "<your_own_value> (source system.interface.name)"
              pbr_map:
                  -
                      comments: "<your_own_value>"
                      name: "default_name_20"
                      rule:
                          -
                              dst: "<your_own_value>"
                              nexthop_group_name: "<your_own_value>"
                              nexthop_ip: "<your_own_value>"
                              nexthop_vrf_name: "<your_own_value> (source router.vrf.name)"
                              seq_num: "<you_own_value>"
                              src: "<your_own_value>"
              protocol: "127"
              seq_num: "<you_own_value>"
              src: "<your_own_value>"
              start_port: "32767"
              tos: "<your_own_value>"
              tos_mask: "<your_own_value>"


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
