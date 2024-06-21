:source: fortiswitch_router_ospf6.py

:orphan:

.. fortiswitch_router_ospf6:

fortiswitch_router_ospf6 -- Router OSPF6 configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and ospf6 category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_ospf6</td>
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
    <li> <span class="li-head">router_ospf6</span> - Router OSPF6 configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">area</span> - OSPF6 area configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">filter_list</span> - OSPF area filter-list configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">direction</span> - Direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
                <li> <span class="li-head">id</span> - Filter list entry ID. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">list</span> - Access-list or prefix-list name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">id</span> - Area entry ip address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">range</span> - OSPF6 area range configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">advertise</span> - Enable/disable advertise status. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
                <li> <span class="li-head">id</span> - Range entry id. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">prefix6</span> - <prefix6>   IPv6 prefix <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">stub_type</span> - Stub summary setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: no-summary, summary</span> </li>
            <li> <span class="li-head">type</span> - Area type setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: regular, stub</span> </li>
            </ul>
        <li> <span class="li-head">interface</span> - OSPF6 interface configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">area_id</span> - A.B.C.D, in IPv4 address format. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">bfd</span> - Enable/Disable Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">cost</span> - The cost of the interface. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">dead_interval</span> - Dead interval. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_interval</span> - Hello interval. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">passive</span> - Enable/disable passive interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">priority</span> - Router priority. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">retransmit_interval</span> - Time between retransmitting lost link state advertisements. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">status</span> - Enable/disable OSPF6 routing on this interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">transmit_delay</span> - Link state transmit delay. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">log_neighbor_changes</span> - Enable logging of OSPF neighbor"s changes. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">redistribute</span> - Redistribute configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">metric</span> - Redistribute metric setting. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">metric_type</span> - metric type <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
            <li> <span class="li-head">name</span> - Redistribute name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">routemap</span> - Route map name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">router_id</span> - A.B.C.D, in IPv4 address format. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">spf_timers</span> - SPF calculation frequency. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Router OSPF6 configuration.
      fortinet.fortiswitch.fortiswitch_router_ospf6:
          router_ospf6:
              area:
                  -
                      filter_list:
                          -
                              direction: "in"
                              id: "6"
                              list: "<your_own_value> (source router.access-list6.name router.prefix-list6.name)"
                      id: "8"
                      range:
                          -
                              advertise: "disable"
                              id: "11"
                              prefix6: "<your_own_value>"
                      stub_type: "no-summary"
                      type: "regular"
              interface:
                  -
                      area_id: "<your_own_value>"
                      bfd: "enable"
                      cost: "18"
                      dead_interval: "19"
                      hello_interval: "20"
                      name: "default_name_21 (source system.interface.name)"
                      passive: "enable"
                      priority: "23"
                      retransmit_interval: "24"
                      status: "disable"
                      transmit_delay: "26"
              log_neighbor_changes: "enable"
              redistribute:
                  -
                      metric: "29"
                      metric_type: "1"
                      name: "default_name_31"
                      routemap: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
              router_id: "<your_own_value>"
              spf_timers: "<your_own_value>"


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
