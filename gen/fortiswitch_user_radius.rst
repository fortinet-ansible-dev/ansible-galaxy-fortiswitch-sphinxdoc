:source: fortiswitch_user_radius.py

:orphan:

.. fortiswitch_user_radius:

fortiswitch_user_radius -- RADIUS server entry configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify user feature and radius category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_user_radius</td>
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
    <li> <span class="li-head">user_radius</span> - RADIUS server entry configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">acct_fast_framedip_detect</span> - Time in seconds ( ) for Accounting message Framed-IP detection from DHCP Snooping. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">acct_interim_interval</span> - Time in seconds ( ) between each accounting interim update message. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">acct_server</span> - Additional accounting servers. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - ID (0 - 4294967295). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">port</span> - RADIUS accounting port number. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">secret</span> - Secret key. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">server</span> - Server IP address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - Enable/disable Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">addr_mode</span> - Address mode (IPv4 or IPv6). <span class="li-normal">type: str</span> <span class="li-normal">choices: ipv4, ipv6</span> </li>
        <li> <span class="li-head">all_usergroup</span> - Enable/disable automatic inclusion of this RADIUS server to all user groups. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">auth_type</span> - Authentication protocol. <span class="li-normal">type: str</span> <span class="li-normal">choices: auto, ms_chap_v2, ms_chap, chap, pap</span> </li>
        <li> <span class="li-head">frame_mtu_size</span> - Frame MTU Size. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">link_monitor</span> - Enable/disable RADIUS link-monitor service from this server. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">link_monitor_interval</span> - Time in seconds ( ) for the link-monitor interval <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">name</span> - RADIUS server entry name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">nas_ip</span> - NAS IPv4 for the RADIUS request. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">nas_ip6</span> - NAS IPv6 for the RADIUS request. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">radius_coa</span> - Enable/disable RADIUS CoA services from this server. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">radius_coa_secret</span> - Secret key to access the local Radius CoA server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">radius_port</span> - Local RADIUS service port number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">secondary_secret</span> - Secret key to access the secondary server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">secondary_server</span> - Secondary RADIUS domain name or IP address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">secret</span> - Secret key to access the primary server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">server</span> - Primary server domain name or IP address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">service_type</span> - Radius Service Type. <span class="li-normal">type: str</span> <span class="li-normal">choices: login, framed, callback-login, callback-framed, outbound, administrative, nas-prompt, authenticate-only, callback-nas-prompt, call-check, callback-administrative</span> </li>
        <li> <span class="li-head">source_ip</span> - Source IPv4 for communications to RADIUS server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">source_ip6</span> - Source IPv6 for communications to RADIUS server. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: RADIUS server entry configuration.
      fortinet.fortiswitch.fortiswitch_user_radius:
          state: "present"
          user_radius:
              acct_fast_framedip_detect: "300"
              acct_interim_interval: "43200"
              acct_server:
                  -
                      id: "6"
                      port: "7"
                      secret: "<your_own_value>"
                      server: "192.168.100.40"
                      status: "enable"
              addr_mode: "ipv4"
              all_usergroup: "disable"
              auth_type: "auto"
              frame_mtu_size: "750"
              link_monitor: "disable"
              link_monitor_interval: "60"
              name: "default_name_17"
              nas_ip: "<your_own_value>"
              nas_ip6: "<your_own_value>"
              radius_coa: "disable"
              radius_coa_secret: "<your_own_value>"
              radius_port: "22"
              secondary_secret: "<your_own_value>"
              secondary_server: "<your_own_value>"
              secret: "<your_own_value>"
              server: "192.168.100.40"
              service_type: "login"
              source_ip: "<your_own_value>"
              source_ip6: "<your_own_value>"


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
