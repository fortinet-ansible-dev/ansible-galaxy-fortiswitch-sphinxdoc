:source: fortiswitch_system_link_monitor.py

:orphan:

.. fortiswitch_system_link_monitor:

fortiswitch_system_link_monitor -- Configure Link Health Monitor in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and link_monitor category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_link_monitor</td>
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
    <li> <span class="li-head">system_link_monitor</span> - Configure Link Health Monitor. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">addr_mode</span> - Address mode (IPv4 or IPv6). <span class="li-normal">type: str</span> <span class="li-normal">choices: ipv4, ipv6</span> </li>
        <li> <span class="li-head">failtime</span> - Number of retry attempts before bringing server down. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">gateway_ip</span> - Gateway IP used to PING the server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">gateway_ip6</span> - Gateway IPv6 address used to PING the server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">http_get</span> - HTTP GET URL string. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">http_match</span> - Response value from detected server in http-get. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">interval</span> - Detection interval. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">name</span> - Link monitor name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">packet_size</span> - Packet size of a twamp test session,. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">password</span> - Twamp controller password in authentication mode. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">port</span> - Port number to poll. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">protocol</span> - Protocols used to detect the server. <span class="li-normal">type: list</span> <span class="li-normal">choices: arp, ping, ping6</span> </li>
        <li> <span class="li-head">recoverytime</span> - Number of retry attempts before bringing server up. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">security_mode</span> - Twamp controller security mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, authentication</span> </li>
        <li> <span class="li-head">server</span> - Server address(es). <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">address</span> - Server address. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">source_ip</span> - Source IP used in packet to the server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">source_ip6</span> - Source IPv6 address used in packet to the server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">srcintf</span> - Interface where the monitor traffic is sent. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable link monitor administrative status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">timeout</span> - Detect request timeout. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">update_cascade_interface</span> - Enable/disable update cascade interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">update_static_route</span> - Enable/disable update static route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Configure Link Health Monitor.
      fortinet.fortiswitch.fortiswitch_system_link_monitor:
          state: "present"
          system_link_monitor:
              addr_mode: "ipv4"
              failtime: "4"
              gateway_ip: "<your_own_value>"
              gateway_ip6: "<your_own_value>"
              http_get: "<your_own_value>"
              http_match: "<your_own_value>"
              interval: "9"
              name: "default_name_10"
              packet_size: "11"
              password: "<your_own_value>"
              port: "13"
              protocol: "arp"
              recoverytime: "15"
              security_mode: "none"
              server:
                  -
                      address: "<your_own_value>"
              source_ip: "<your_own_value>"
              source_ip6: "<your_own_value>"
              srcintf: "<your_own_value> (source system.interface.name)"
              status: "enable"
              timeout: "23"
              update_cascade_interface: "enable"
              update_static_route: "enable"


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
