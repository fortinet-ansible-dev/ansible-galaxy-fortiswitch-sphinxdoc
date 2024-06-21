:source: fortiswitch_system_dhcp_server.py

:orphan:

.. fortiswitch_system_dhcp_server:

fortiswitch_system_dhcp_server -- Configure DHCP servers in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system_dhcp feature and server category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_dhcp_server</td>
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
    <li> <span class="li-head">system_dhcp_server</span> - Configure DHCP servers. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">auto_configuration</span> - Enable/disable auto configuration. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">conflicted_ip_timeout</span> - Time in seconds to wait after a conflicted IP address is removed from the DHCP range before it can be reused. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">default_gateway</span> - Default gateway IP address assigned by the DHCP server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dns_server1</span> - DNS server 1. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dns_server2</span> - DNS server 2. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dns_server3</span> - DNS server 3. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dns_service</span> - Options for assigning DNS servers to DHCP clients. <span class="li-normal">type: str</span> <span class="li-normal">choices: local, default, specify</span> </li>
        <li> <span class="li-head">domain</span> - Domain name suffix for the IP addresses that the DHCP server assigns to clients. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">exclude_range</span> - Exclude one or more ranges of IP addresses from being assigned to clients. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">end_ip</span> - End of IP range. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">start_ip</span> - Start of IP range. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">filename</span> - Name of the boot file on the TFTP server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">interface</span> - DHCP server can assign IP configurations to clients connected to this interface. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip_mode</span> - Method used to assign client IP. <span class="li-normal">type: str</span> <span class="li-normal">choices: range, usrgrp</span> </li>
        <li> <span class="li-head">ip_range</span> - DHCP IP range configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">end_ip</span> - End of IP range. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">start_ip</span> - Start of IP range. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">lease_time</span> - Lease time in seconds, 0 means unlimited. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">netmask</span> - Netmask assigned by the DHCP server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">next_server</span> - IP address of a server (for example, a TFTP sever) that DHCP clients can download a boot file from. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ntp_server1</span> - NTP server 1. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ntp_server2</span> - NTP server 2. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ntp_server3</span> - NTP server 3. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ntp_service</span> - Options for assigning Network Time Protocol (NTP) servers to DHCP clients. <span class="li-normal">type: str</span> <span class="li-normal">choices: local, default, specify</span> </li>
        <li> <span class="li-head">options</span> - DHCP options. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">code</span> - DHCP option code. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip</span> - DHCP option IPs. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">type</span> - DHCP option type. <span class="li-normal">type: str</span> <span class="li-normal">choices: hex, string, ip, fqdn</span> </li>
            <li> <span class="li-head">value</span> - DHCP option value. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">reserved_address</span> - Options for the DHCP server to assign IP settings to specific MAC addresses. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">action</span> - Options for the DHCP server to configure the client with the reserved MAC address. <span class="li-normal">type: str</span> <span class="li-normal">choices: assign, block, reserved</span> </li>
            <li> <span class="li-head">circuit_id</span> - Option 82 circuit-ID of the client that will get the reserved IP address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">circuit_id_type</span> - DHCP option type. <span class="li-normal">type: str</span> <span class="li-normal">choices: hex, string</span> </li>
            <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip</span> - IP address to be reserved for the MAC address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">mac</span> - MAC address of the client that will get the reserved IP address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">remote_id</span> - Option 82 remote-ID of the client that will get the reserved IP address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">remote_id_type</span> - DHCP option type. <span class="li-normal">type: str</span> <span class="li-normal">choices: hex, string</span> </li>
            <li> <span class="li-head">type</span> - DHCP reserved-address type. <span class="li-normal">type: str</span> <span class="li-normal">choices: mac, option82</span> </li>
            </ul>
        <li> <span class="li-head">server_type</span> - DHCP server can be a normal DHCP server or an IPsec DHCP server. <span class="li-normal">type: str</span> <span class="li-normal">choices: regular</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable this DHCP configuration. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">tftp_server</span> - One or more hostnames or IP addresses of the TFTP servers in quotes separated by spaces. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">tftp_server</span> - TFTP server. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">timezone</span> - Select the time zone to be assigned to DHCP clients. <span class="li-normal">type: str</span> <span class="li-normal">choices: 01, 02, 03, 04, 05, 81, 06, 07, 08, 09, 10, 11, 12, 13, 74, 14, 77, 15, 87, 16, 17, 18, 19, 20, 75, 21, 22, 23, 24, 80, 79, 25, 26, 27, 28, 78, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 83, 84, 40, 85, 41, 42, 43, 39, 44, 46, 47, 51, 48, 45, 49, 50, 52, 53, 54, 55, 56, 57, 58, 59, 60, 62, 63, 61, 64, 65, 66, 67, 68, 69, 70, 71, 72, 00, 82, 73, 86, 76, 88, 89, 90, 91, 92</span> </li>
        <li> <span class="li-head">timezone_option</span> - Options for the DHCP server to set the client"s time zone. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, default, specify</span> </li>
        <li> <span class="li-head">vci_match</span> - Enable/disable vendor class identifier (VCI) matching. When enabled only DHCP requests with a matching VCI are served. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">vci_string</span> - One or more VCI strings in quotes separated by spaces. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">vci_string</span> - VCI strings. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">wifi_ac1</span> - WiFi Access Controller 1 IP address (DHCP option 138, RFC 5417). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">wifi_ac2</span> - WiFi Access Controller 2 IP address (DHCP option 138, RFC 5417). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">wifi_ac3</span> - WiFi Access Controller 3 IP address (DHCP option 138, RFC 5417). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">wins_server1</span> - WINS server 1. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">wins_server2</span> - WINS server 2. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Configure DHCP servers.
      fortinet.fortiswitch.fortiswitch_system_dhcp_server:
          state: "present"
          system_dhcp_server:
              auto_configuration: "disable"
              conflicted_ip_timeout: "4"
              default_gateway: "<your_own_value>"
              dns_server1: "<your_own_value>"
              dns_server2: "<your_own_value>"
              dns_server3: "<your_own_value>"
              dns_service: "local"
              domain: "<your_own_value>"
              exclude_range:
                  -
                      end_ip: "<your_own_value>"
                      id: "13"
                      start_ip: "<your_own_value>"
              filename: "<your_own_value>"
              id: "16"
              interface: "<your_own_value> (source system.interface.name)"
              ip_mode: "range"
              ip_range:
                  -
                      end_ip: "<your_own_value>"
                      id: "21"
                      start_ip: "<your_own_value>"
              lease_time: "23"
              netmask: "<your_own_value>"
              next_server: "<your_own_value>"
              ntp_server1: "<your_own_value>"
              ntp_server2: "<your_own_value>"
              ntp_server3: "<your_own_value>"
              ntp_service: "local"
              options:
                  -
                      code: "31"
                      id: "32"
                      ip: "<your_own_value>"
                      type: "hex"
                      value: "<your_own_value>"
              reserved_address:
                  -
                      action: "assign"
                      circuit_id: "<your_own_value>"
                      circuit_id_type: "hex"
                      description: "<your_own_value>"
                      id: "41"
                      ip: "<your_own_value>"
                      mac: "<your_own_value>"
                      remote_id: "<your_own_value>"
                      remote_id_type: "hex"
                      type: "mac"
              server_type: "regular"
              status: "disable"
              tftp_server:
                  -
                      tftp_server: "<your_own_value>"
              timezone: "01"
              timezone_option: "disable"
              vci_match: "disable"
              vci_string:
                  -
                      vci_string: "<your_own_value>"
              wifi_ac1: "<your_own_value>"
              wifi_ac2: "<your_own_value>"
              wifi_ac3: "<your_own_value>"
              wins_server1: "<your_own_value>"
              wins_server2: "<your_own_value>"


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
