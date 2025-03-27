:source: fortiswitch_router_ospf.py

:orphan:

.. fortiswitch_router_ospf:

fortiswitch_router_ospf -- OSPF configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and ospf category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_ospf</td>
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
    <li> <span class="li-head">router_ospf</span> - OSPF configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">abr_type</span> - Area border router type. <span class="li-normal">type: str</span> <span class="li-normal">choices: cisco, ibm, shortcut, standard</span> </li>
        <li> <span class="li-head">area</span> - OSPF area configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">default_cost</span> - Summary default cost of stub or NSSA area. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">filter_list</span> - OSPF area filter-list configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">direction</span> - Direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
                <li> <span class="li-head">id</span> - Filter list entry ID. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">list</span> - Access-list or prefix-list name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">id</span> - Area entry IP address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">nssa_translator_role</span> - NSSA translator role type. <span class="li-normal">type: str</span> <span class="li-normal">choices: candidate, never, always</span> </li>
            <li> <span class="li-head">range</span> - OSPF area range configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">advertise</span> - Enable/disable advertise status. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
                <li> <span class="li-head">id</span> - Range entry ID. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">prefix</span> - Prefix. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">substitute</span> - Substitute prefix. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">substitute_status</span> - Enable/disable substitute status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                </ul>
            <li> <span class="li-head">shortcut</span> - Enable/disable shortcut option. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable, default</span> </li>
            <li> <span class="li-head">stub_type</span> - Stub summary setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: no-summary, summary</span> </li>
            <li> <span class="li-head">type</span> - Area type setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: regular, nssa, stub</span> </li>
            <li> <span class="li-head">virtual_link</span> - OSPF virtual link configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">authentication</span> - Authentication type. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, text, md5</span> </li>
                <li> <span class="li-head">authentication_key</span> - Authentication key. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">dead_interval</span> - Dead interval. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">hello_interval</span> - Hello interval. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">md5_keys</span> - OSPF md5 key configuration. Applicable only when authentication field is set to md5. <span class="li-normal">type: list</span> </li>
                    <ul class="ul-self">
                    <li> <span class="li-head">id</span> - key-id (1-255). <span class="li-normal">type: int</span> </li>
                    <li> <span class="li-head">key</span> - md5-key. <span class="li-normal">type: str</span> </li>
                    </ul>
                <li> <span class="li-head">name</span> - Virtual link entry name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">peer</span> - Peer IP. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">retransmit_interval</span> - Time between retransmitting lost link state advertisements. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">transmit_delay</span> - Link state transmit delay. <span class="li-normal">type: int</span> </li>
                </ul>
            </ul>
        <li> <span class="li-head">database_overflow</span> - Enable/disable database overflow. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">database_overflow_max_external_lsa</span> - Database overflow maximum External LSAs. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">database_overflow_time_to_recover</span> - Database overflow time to recover (sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">default_information_metric</span> - Default information metric. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">default_information_metric_type</span> - Default information metric type. <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
        <li> <span class="li-head">default_information_originate</span> - Enable/disable generation of default route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, always, disable</span> </li>
        <li> <span class="li-head">distance</span> - Administrative distance. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distance_external</span> - Administrative external route distance. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distance_inter_area</span> - Administrative inter-area route distance. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distance_intra_area</span> - Administrative intra-area route distance. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distribute_list</span> - Redistribute routes filter. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">access_list</span> - Access list name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - Distribute list entry ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">protocol</span> - Protocol type. <span class="li-normal">type: str</span> <span class="li-normal">choices: connected, static, rip, bgp, isis</span> </li>
            </ul>
        <li> <span class="li-head">interface</span> - OSPF interface configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">authentication</span> - Authentication type. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, text, md5</span> </li>
            <li> <span class="li-head">authentication_key</span> - Authentication key. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">bfd</span> - Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">cost</span> - Cost of the interface. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">dead_interval</span> - Dead interval. For fast-hello assign value 1. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_interval</span> - Hello interval. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_multiplier</span> - Number of hello packets within dead interval.Valid only for fast-hello. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">md5_keys</span> - OSPF md5 key configuration. Applicable only when authentication field is set to md5. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">id</span> - key-id (1-255). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">key</span> - md5-key. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">mtu</span> - Interface MTU. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">mtu_ignore</span> - Disable MTU mismatch detection on this interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">name</span> - Interface entry name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">priority</span> - Router priority. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">retransmit_interval</span> - Time between retransmitting lost link state advertisements. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">transmit_delay</span> - Link state transmit delay. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ttl</span> - TTL. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ucast_ttl</span> - Unicast TTL. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">log_neighbour_changes</span> - Enable logging of OSPF neighbour"s changes <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">name</span> - Vrf name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">network</span> - Enable OSPF on an IP network. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">area</span> - Attach the network to area. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - Network entry ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix</span> - Prefix. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">passive_interface</span> - Passive interface configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Passive interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">redistribute</span> - Redistribute configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">metric</span> - Redistribute metric setting. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">metric_type</span> - Metric type. <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
            <li> <span class="li-head">name</span> - Redistribute name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">routemap</span> - Route map name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">tag</span> - Tag value. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">rfc1583_compatible</span> - Enable/disable RFC1583 compatibility. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">router_id</span> - Router ID. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">spf_timers</span> - SPF calculation frequency. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">summary_address</span> - Aggregate address for redistributed routes. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Summary address entry ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix</span> - Prefix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">tag</span> - Tag value. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">vrf</span> - Enable OSPF on VRF. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">abr_type</span> - Area border router type. <span class="li-normal">type: str</span> <span class="li-normal">choices: cisco, ibm, shortcut, standard</span> </li>
            <li> <span class="li-head">area</span> - OSPF area configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">default_cost</span> - Summary default cost of stub or NSSA area. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">filter_list</span> - OSPF area filter-list configuration. <span class="li-normal">type: list</span> </li>
                    <ul class="ul-self">
                    <li> <span class="li-head">direction</span> - Direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
                    <li> <span class="li-head">id</span> - Filter list entry ID. <span class="li-normal">type: int</span> </li>
                    <li> <span class="li-head">list</span> - Access-list or prefix-list name. <span class="li-normal">type: str</span> </li>
                    </ul>
                <li> <span class="li-head">id</span> - Area entry IP address. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">nssa_translator_role</span> - NSSA translator role type. <span class="li-normal">type: str</span> <span class="li-normal">choices: candidate, never, always</span> </li>
                <li> <span class="li-head">range</span> - OSPF area range configuration. <span class="li-normal">type: list</span> </li>
                    <ul class="ul-self">
                    <li> <span class="li-head">advertise</span> - Enable/disable advertise status. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
                    <li> <span class="li-head">id</span> - Range entry ID. <span class="li-normal">type: int</span> </li>
                    <li> <span class="li-head">prefix</span> - Prefix. <span class="li-normal">type: str</span> </li>
                    <li> <span class="li-head">substitute</span> - Substitute prefix. <span class="li-normal">type: str</span> </li>
                    <li> <span class="li-head">substitute_status</span> - Enable/disable substitute status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                    </ul>
                <li> <span class="li-head">shortcut</span> - Enable/disable shortcut option. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable, default</span> </li>
                <li> <span class="li-head">stub_type</span> - Stub summary setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: no-summary, summary</span> </li>
                <li> <span class="li-head">type</span> - Area type setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: regular, nssa, stub</span> </li>
                <li> <span class="li-head">virtual_link</span> - OSPF virtual link configuration. <span class="li-normal">type: list</span> </li>
                    <ul class="ul-self">
                    <li> <span class="li-head">authentication</span> - Authentication type. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, text</span> </li>
                    <li> <span class="li-head">authentication_key</span> - Authentication key. <span class="li-normal">type: str</span> </li>
                    <li> <span class="li-head">dead_interval</span> - Dead interval. <span class="li-normal">type: int</span> </li>
                    <li> <span class="li-head">hello_interval</span> - Hello interval. <span class="li-normal">type: int</span> </li>
                    <li> <span class="li-head">name</span> - Virtual link entry name. <span class="li-normal">type: str</span> </li>
                    <li> <span class="li-head">peer</span> - Peer IP. <span class="li-normal">type: str</span> </li>
                    <li> <span class="li-head">retransmit_interval</span> - Time between retransmitting lost link state advertisements. <span class="li-normal">type: int</span> </li>
                    <li> <span class="li-head">transmit_delay</span> - Link state transmit delay. <span class="li-normal">type: int</span> </li>
                    </ul>
                </ul>
            <li> <span class="li-head">database_overflow</span> - Enable/disable database overflow. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">database_overflow_max_external_lsa</span> - Database overflow maximum External LSAs. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">database_overflow_time_to_recover</span> - Database overflow time to recover (sec). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">default_information_metric</span> - Default information metric. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">default_information_metric_type</span> - Default information metric type. <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
            <li> <span class="li-head">default_information_originate</span> - Enable/disable generation of default route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, always, disable</span> </li>
            <li> <span class="li-head">distance</span> - Administrative distance. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">distance_external</span> - Administrative external route distance. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">distance_inter_area</span> - Administrative inter-area route distance. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">distance_intra_area</span> - Administrative intra-area route distance. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">distribute_list</span> - Redistribute routes filter. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">access_list</span> - Access list name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">id</span> - Distribute list entry ID. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">protocol</span> - Protocol type. <span class="li-normal">type: str</span> <span class="li-normal">choices: connected, static, rip, bgp, isis</span> </li>
                </ul>
            <li> <span class="li-head">interface</span> - OSPF interface configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">authentication</span> - Authentication type. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, text, md5</span> </li>
                <li> <span class="li-head">authentication_key</span> - Authentication key. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">cost</span> - Cost of the interface. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">dead_interval</span> - Dead interval. For fast-hello assign value 1. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">hello_interval</span> - Hello interval. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">hello_multiplier</span> - Number of hello packets within dead interval.Valid only for fast-hello. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">md5_keys</span> - OSPF md5 key configuration. Applicable only when authentication field is set to md5. <span class="li-normal">type: list</span> </li>
                    <ul class="ul-self">
                    <li> <span class="li-head">id</span> - key-id (1-255). <span class="li-normal">type: int</span> </li>
                    <li> <span class="li-head">key</span> - md5-key. <span class="li-normal">type: str</span> </li>
                    </ul>
                <li> <span class="li-head">mtu</span> - Interface MTU. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">mtu_ignore</span> - Disable MTU mismatch detection on this interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">name</span> - Interface entry name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">priority</span> - Router priority. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">retransmit_interval</span> - Time between retransmitting lost link state advertisements. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">transmit_delay</span> - Link state transmit delay. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">ttl</span> - TTL. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">ucast_ttl</span> - Unicast TTL. <span class="li-normal">type: int</span> </li>
                </ul>
            <li> <span class="li-head">log_neighbour_changes</span> - Enable logging of OSPF neighbour"s changes <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">name</span> - Vrf name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">network</span> - Enable OSPF on an IP network. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">area</span> - Attach the network to area. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">id</span> - Network entry ID. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">prefix</span> - Prefix. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">passive_interface</span> - Passive interface configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">name</span> - Passive interface name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">redistribute</span> - Redistribute configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">metric</span> - Redistribute metric setting. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">metric_type</span> - Metric type. <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
                <li> <span class="li-head">name</span> - Redistribute name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">routemap</span> - Route map name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">status</span> - status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                <li> <span class="li-head">tag</span> - Tag value. <span class="li-normal">type: int</span> </li>
                </ul>
            <li> <span class="li-head">rfc1583_compatible</span> - Enable/disable RFC1583 compatibility. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">router_id</span> - Router ID. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">spf_timers</span> - SPF calculation frequency. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">summary_address</span> - Aggregate address for redistributed routes. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">id</span> - Summary address entry ID. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">prefix</span> - Prefix. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">tag</span> - Tag value. <span class="li-normal">type: int</span> </li>
                </ul>
            </ul>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: OSPF configuration.
      fortinet.fortiswitch.fortiswitch_router_ospf:
          router_ospf:
              abr_type: "cisco"
              area:
                  -
                      default_cost: "1073741823"
                      filter_list:
                          -
                              direction: "in"
                              id: "8"
                              list: "<your_own_value> (source router.access-list.name router.prefix-list.name)"
                      id: "10"
                      nssa_translator_role: "candidate"
                      range:
                          -
                              advertise: "disable"
                              id: "14"
                              prefix: "<your_own_value>"
                              substitute: "<your_own_value>"
                              substitute_status: "enable"
                      shortcut: "disable"
                      stub_type: "no-summary"
                      type: "regular"
                      virtual_link:
                          -
                              authentication: "none"
                              authentication_key: "<your_own_value>"
                              dead_interval: "24"
                              hello_interval: "25"
                              md5_keys:
                                  -
                                      id: "27"
                                      key: "<your_own_value>"
                              name: "default_name_29"
                              peer: "<your_own_value>"
                              retransmit_interval: "31"
                              transmit_delay: "32"
              database_overflow: "enable"
              database_overflow_max_external_lsa: "1073741823"
              database_overflow_time_to_recover: "35"
              default_information_metric: "36"
              default_information_metric_type: "1"
              default_information_originate: "enable"
              distance: "39"
              distance_external: "40"
              distance_inter_area: "41"
              distance_intra_area: "42"
              distribute_list:
                  -
                      access_list: "<your_own_value> (source router.access-list.name)"
                      id: "45"
                      protocol: "connected"
              interface:
                  -
                      authentication: "none"
                      authentication_key: "<your_own_value>"
                      bfd: "enable"
                      cost: "51"
                      dead_interval: "52"
                      hello_interval: "53"
                      hello_multiplier: "54"
                      md5_keys:
                          -
                              id: "56"
                              key: "<your_own_value>"
                      mtu: "58"
                      mtu_ignore: "enable"
                      name: "default_name_60 (source system.interface.name)"
                      priority: "61"
                      retransmit_interval: "62"
                      transmit_delay: "63"
                      ttl: "127"
                      ucast_ttl: "65"
              log_neighbour_changes: "enable"
              name: "default_name_67"
              network:
                  -
                      area: "<your_own_value>"
                      id: "70"
                      prefix: "<your_own_value>"
              passive_interface:
                  -
                      name: "default_name_73 (source system.interface.name)"
              redistribute:
                  -
                      metric: "75"
                      metric_type: "1"
                      name: "default_name_77"
                      routemap: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
                      tag: "1073741823"
              rfc1583_compatible: "enable"
              router_id: "<your_own_value>"
              spf_timers: "<your_own_value>"
              summary_address:
                  -
                      id: "85"
                      prefix: "<your_own_value>"
                      tag: "1073741823"
              vrf:
                  -
                      abr_type: "cisco"
                      area:
                          -
                              default_cost: "1073741823"
                              filter_list:
                                  -
                                      direction: "in"
                                      id: "94"
                                      list: "<your_own_value> (source router.access-list.name router.prefix-list.name)"
                              id: "96"
                              nssa_translator_role: "candidate"
                              range:
                                  -
                                      advertise: "disable"
                                      id: "100"
                                      prefix: "<your_own_value>"
                                      substitute: "<your_own_value>"
                                      substitute_status: "enable"
                              shortcut: "disable"
                              stub_type: "no-summary"
                              type: "regular"
                              virtual_link:
                                  -
                                      authentication: "none"
                                      authentication_key: "<your_own_value>"
                                      dead_interval: "110"
                                      hello_interval: "111"
                                      name: "default_name_112"
                                      peer: "<your_own_value>"
                                      retransmit_interval: "114"
                                      transmit_delay: "115"
                      database_overflow: "enable"
                      database_overflow_max_external_lsa: "1073741823"
                      database_overflow_time_to_recover: "118"
                      default_information_metric: "119"
                      default_information_metric_type: "1"
                      default_information_originate: "enable"
                      distance: "122"
                      distance_external: "123"
                      distance_inter_area: "124"
                      distance_intra_area: "125"
                      distribute_list:
                          -
                              access_list: "<your_own_value> (source router.access-list.name)"
                              id: "128"
                              protocol: "connected"
                      interface:
                          -
                              authentication: "none"
                              authentication_key: "<your_own_value>"
                              cost: "133"
                              dead_interval: "134"
                              hello_interval: "135"
                              hello_multiplier: "136"
                              md5_keys:
                                  -
                                      id: "138"
                                      key: "<your_own_value>"
                              mtu: "140"
                              mtu_ignore: "enable"
                              name: "default_name_142 (source system.interface.name)"
                              priority: "143"
                              retransmit_interval: "144"
                              transmit_delay: "145"
                              ttl: "127"
                              ucast_ttl: "147"
                      log_neighbour_changes: "enable"
                      name: "default_name_149 (source router.vrf.name)"
                      network:
                          -
                              area: "<your_own_value>"
                              id: "152"
                              prefix: "<your_own_value>"
                      passive_interface:
                          -
                              name: "default_name_155 (source system.interface.name)"
                      redistribute:
                          -
                              metric: "157"
                              metric_type: "1"
                              name: "default_name_159"
                              routemap: "<your_own_value> (source router.route-map.name)"
                              status: "enable"
                              tag: "1073741823"
                      rfc1583_compatible: "enable"
                      router_id: "<your_own_value>"
                      spf_timers: "<your_own_value>"
                      summary_address:
                          -
                              id: "167"
                              prefix: "<your_own_value>"
                              tag: "1073741823"


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
