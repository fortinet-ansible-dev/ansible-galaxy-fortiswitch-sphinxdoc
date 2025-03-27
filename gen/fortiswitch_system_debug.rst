:source: fortiswitch_system_debug.py

:orphan:

.. fortiswitch_system_debug:

fortiswitch_system_debug -- Application and CLI debug values to set at startup and retain over reboot in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and debug category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td></td><td colspan="0">Supported Version Ranges</td>
 </tr>
 <tr>
 <td>fortiswitch_system_debug</td>
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
    <li> <span class="li-head">system_debug</span> - Application and CLI debug values to set at startup and retain over reboot. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">alertd</span> - Monitor and Alert daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">apache</span> - Apache. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">auto_script</span> - Auto script. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">autod</span> - Automation Stitches. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bfdd</span> - Bidirectional Forwarding Detection (BFD) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bgpd</span> - Bgp daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">cli</span> - CMDB/CLI debug. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ctrld</span> - Switch general control daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">cu_swtpd</span> - Switch-controller CAPWAP daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">delayclid</span> - Delay CLI daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcp6c</span> - DHCPv6 client. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcpc</span> - DHCP client module. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcprelay</span> - DHCP relay daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcps</span> - DHCP server. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dmid</span> - DMI daemon debug. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dnsproxy</span> - DNS proxy module. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">eap_proxy</span> - EAP proxy daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">email_server</span> - Email server. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">erspan_auto_mgr</span> - ERSPAN-auto mode configuration resolution daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">flan_mgr</span> - FortiLAN Cloud Manager daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">flcmdd</span> - FortiLink command daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">flow_export</span> - Flow-export debug. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">fnbamd</span> - Fortigate non-blocking auth daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">fortilinkd</span> - FortiLink daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">fpmd</span> - FPMD HW routing daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">gratarp</span> - IP Conflict Gratuitious ARP utility. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">gui</span> - GUI service. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">gvrpd</span> - GVRP daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">httpsd</span> - HTTP/HTTPS daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ip6addrd</span> - IPv6 address utility. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ipconflictd</span> - IP Conflictd detection daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">isisd</span> - Isis daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">l2d</span> - L2 daemon responsible to have core logic to assist L2 feature like MCLAG. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">l2dbg</span> - Background daemon responsible to assist in any heavy HW related operation needed by L2d. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">l3</span> - L3 debug. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lacpd</span> - Link Aggregation Control Protocol (LACP) debug. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">libswitchd</span> - Switch library daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">link_monitor</span> - Link monitor daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lldpmedd</span> - Link Layer Discovery Protocol (LLDP) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">macsec_srv</span> - MKA/Fortilink macsec cak server daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mcast_snooping</span> - Multicast Snooping debug. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">miglogd</span> - Log daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ntpd</span> - Network Time Protocol (NTP) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">nwmcfgd</span> - Network monitor daemon responsible for handling configuration. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">nwmonitord</span> - Network monitor daemon responsible for packet handling and parsing. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ospf6d</span> - Open Shortest Path First (OSPFv6) routing daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ospfd</span> - Open Shortest Path First (OSPF) routing daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">pbrd</span> - Policy Based Routing (PBR) routing daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">pimd</span> - Protocol Independent Multicast (PIM) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">portspeedd</span> - Port speed daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">radius_das</span> - Radius CoA daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">radvd</span> - router adv daemon <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">raguard</span> - raguard daemon <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ripd</span> - Routing Information Protocol (RIP) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ripngd</span> - Routing Information Protocol NG (RIPNG) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">router_launcher</span> - Routing system launcher daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">rsyslogd</span> - Remote SYSLOG daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">scep</span> - SCEP <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">sflowd</span> - sFlow collection and export daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">snmpd</span> - Simple Network Managment Protocol (SNMP) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">sshd</span> - Secure Sockets Shell(SSH) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">staticd</span> - Static route daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">statsd</span> - Stats collection daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">stpd</span> - Spanning Tree (STP) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">switch_launcher</span> - Switching system launcher daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trunkd</span> - Link Aggregation Control Protocol (LACP) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">vrrpd</span> - Virtual Router Redundancy Protocol (VRRP) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">wiredap</span> - Wired AP (802.1X port-based auth) daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">wpa_supp</span> - MKA/Fortilink macsec daemon. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">zebra</span> - Zebra routing daemon. <span class="li-normal">type: int</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Application and CLI debug values to set at startup and retain over reboot.
      fortinet.fortiswitch.fortiswitch_system_debug:
          system_debug:
              alertd: "3"
              apache: "4"
              auto_script: "5"
              autod: "6"
              bfdd: "7"
              bgpd: "8"
              cli: "4"
              ctrld: "10"
              cu_swtpd: "11"
              delayclid: "12"
              dhcp6c: "13"
              dhcpc: "14"
              dhcprelay: "15"
              dhcps: "16"
              dmid: "17"
              dnsproxy: "18"
              eap_proxy: "19"
              email_server: "20"
              erspan_auto_mgr: "21"
              flan_mgr: "22"
              flcmdd: "23"
              flow_export: "24"
              fnbamd: "25"
              fortilinkd: "26"
              fpmd: "27"
              gratarp: "28"
              gui: "29"
              gvrpd: "30"
              httpsd: "31"
              ip6addrd: "32"
              ipconflictd: "33"
              isisd: "34"
              l2d: "35"
              l2dbg: "36"
              l3: "37"
              lacpd: "38"
              libswitchd: "39"
              link_monitor: "40"
              lldpmedd: "41"
              macsec_srv: "42"
              mcast_snooping: "43"
              miglogd: "44"
              ntpd: "45"
              nwmcfgd: "46"
              nwmonitord: "47"
              ospf6d: "48"
              ospfd: "49"
              pbrd: "50"
              pimd: "51"
              portspeedd: "52"
              radius_das: "53"
              radvd: "54"
              raguard: "55"
              ripd: "56"
              ripngd: "57"
              router_launcher: "58"
              rsyslogd: "59"
              scep: "60"
              sflowd: "61"
              snmpd: "62"
              sshd: "63"
              staticd: "64"
              statsd: "65"
              stpd: "66"
              switch_launcher: "67"
              trunkd: "68"
              vrrpd: "69"
              wiredap: "70"
              wpa_supp: "71"
              zebra: "72"


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
