:source: fortiswitch_system_flow_export.py

:orphan:

.. fortiswitch_system_flow_export:

fortiswitch_system_flow_export -- System Flow Export settings in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and flow_export category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_flow_export</td>
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
    <li> <span class="li-head">system_flow_export</span> - System Flow Export settings. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">aggregates</span> - Aggregates. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Aggregate id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip</span> - Aggregate"s IP and Mask. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">collectors</span> - Collectors. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">ip</span> - IP address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">name</span> - Collector name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">port</span> - Port number (0-65535). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">transport</span> - Export transport (udp|tcp|sctp). <span class="li-normal">type: str</span> <span class="li-normal">choices: udp, tcp, sctp</span> </li>
            </ul>
        <li> <span class="li-head">filter</span> - Filter (BPF). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">format</span> - Export Format (netflow1|netflow5|netflow9|ipfix). <span class="li-normal">type: str</span> <span class="li-normal">choices: netflow1, netflow5, netflow9, ipfix</span> </li>
        <li> <span class="li-head">identity</span> - Set identity of switch (0x00000000-0xFFFFFFFF ). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">level</span> - Export Level (vlan|ip|port|protocol|mac). <span class="li-normal">type: str</span> <span class="li-normal">choices: mac, ip, proto, port, vlan</span> </li>
        <li> <span class="li-head">max_export_pkt_size</span> - Max Export Packet Size (512-9216). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">template_export_period</span> - Template export period in minutes (1-60). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">timeout_general</span> - Flow Session General Timeout (60-604800). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">timeout_icmp</span> - Flow Session ICMP Timeout (60-604800). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">timeout_max</span> - Flow Session MAX Timeout (60-604800). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">timeout_tcp</span> - Flow Session TCP Timeout (60-604800). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">timeout_tcp_fin</span> - Flow Session TCP Fin Timeout (60-604800). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">timeout_tcp_rst</span> - Flow Session TCP Reset Timeout (60-604800). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">timeout_udp</span> - Flow Session UDP Timeout (60-604800). <span class="li-normal">type: int</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: System Flow Export settings.
      fortinet.fortiswitch.fortiswitch_system_flow_export:
          system_flow_export:
              aggregates:
                  -
                      id: "4"
                      ip: "<your_own_value>"
              collectors:
                  -
                      ip: "<your_own_value>"
                      name: "default_name_8"
                      port: "9"
                      transport: "udp"
              filter: "<your_own_value>"
              format: "netflow1"
              identity: "13"
              level: "mac"
              max_export_pkt_size: "15"
              template_export_period: "16"
              timeout_general: "17"
              timeout_icmp: "18"
              timeout_max: "19"
              timeout_tcp: "20"
              timeout_tcp_fin: "21"
              timeout_tcp_rst: "22"
              timeout_udp: "23"


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
