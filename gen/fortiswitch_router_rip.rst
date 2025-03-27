:source: fortiswitch_router_rip.py

:orphan:

.. fortiswitch_router_rip:

fortiswitch_router_rip -- RIP configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and rip category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_rip</td>
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
    <li> <span class="li-head">router_rip</span> - RIP configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">bfd</span> - Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">default_information_originate</span> - Generate a default route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">default_metric</span> - Default metric of redistribute routes (Except connected). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distance</span> - Set admin distance based on route source ip. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">access_list</span> - Access list for route destination. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distance</span> - Distance. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">id</span> - Distance id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix</span> - IP source prefix. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">distribute_list</span> - Filter networks in routing updates. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">direction</span> - Distribute list direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
            <li> <span class="li-head">id</span> - Distribute-list id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Distribute list interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">listname</span> - Distribute access/prefix list name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">garbage_timer</span> - Garbage collection timer. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">interface</span> - RIP interface configuration <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">auth_keychain</span> - Authentication keychain name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">auth_mode</span> - Authentication mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, text, md5</span> </li>
            <li> <span class="li-head">auth_string</span> - Authentication string/password. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">bfd</span> - Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">flags</span> - flags <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - interface name <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">receive_version</span> - Receive version. <span class="li-normal">type: str</span> <span class="li-normal">choices: global, 1, 2, both</span> </li>
            <li> <span class="li-head">send_version</span> - Send version. <span class="li-normal">type: str</span> <span class="li-normal">choices: global, 1, 2, both</span> </li>
            <li> <span class="li-head">send_version2_broadcast</span> - broadcast version 1 compatible packets <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">split_horizon</span> - Split horizon method. <span class="li-normal">type: str</span> <span class="li-normal">choices: poisoned, regular</span> </li>
            <li> <span class="li-head">split_horizon_status</span> - Split horizon status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">name</span> - Vrf name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">neighbor</span> - Specify a neighbor router. Required only for non-multicast networks. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Neighbor entry id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ip</span> - IP address. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">network</span> - Enable RIP routing on an IP network. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Network entry id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix</span> - Network prefix. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">offset_list</span> - Offset list to modify RIP metric. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">access_list</span> - Access list name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">direction</span> - Offset list direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
            <li> <span class="li-head">id</span> - Offset-list id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Interface to match. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">offset</span> - Metric value. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">passive_interface</span> - Passive interface configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Passive interface name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">recv_buffer_size</span> - receiving buffer size <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">redistribute</span> - Redistribute configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">flags</span> - flags <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">metric</span> - Redistribute metric setting. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - Redistribute name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">routemap</span> - Route map name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">timeout_timer</span> - Routing information timeout timer. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">update_timer</span> - Routing table update timer. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">version</span> - RIP version <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
        <li> <span class="li-head">vrf</span> - Enable RIP on VRF. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">default_information_originate</span> - Generate a default route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">default_metric</span> - Default metric of redistribute routes (Except connected). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">distance</span> - Set admin distance based on route source ip. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">access_list</span> - Access list for route destination. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">distance</span> - Distance. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">id</span> - Distance id. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">prefix</span> - IP source prefix. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">distribute_list</span> - Filter networks in routing updates. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">direction</span> - Distribute list direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
                <li> <span class="li-head">id</span> - Distribute-list id. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">interface</span> - Distribute list interface name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">listname</span> - Distribute access/prefix list name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                </ul>
            <li> <span class="li-head">garbage_timer</span> - Garbage collection timer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - RIP interface configuration <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">auth_keychain</span> - Authentication keychain name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">auth_mode</span> - Authentication mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, text, md5</span> </li>
                <li> <span class="li-head">auth_string</span> - Authentication string/password. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">flags</span> - flags <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">name</span> - interface name <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">receive_version</span> - Receive version. <span class="li-normal">type: str</span> <span class="li-normal">choices: global, 1, 2, both</span> </li>
                <li> <span class="li-head">send_version</span> - Send version. <span class="li-normal">type: str</span> <span class="li-normal">choices: global, 1, 2, both</span> </li>
                <li> <span class="li-head">send_version2_broadcast</span> - broadcast version 1 compatible packets <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
                <li> <span class="li-head">split_horizon</span> - Split horizon method. <span class="li-normal">type: str</span> <span class="li-normal">choices: poisoned, regular</span> </li>
                <li> <span class="li-head">split_horizon_status</span> - Split horizon status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                </ul>
            <li> <span class="li-head">name</span> - Vrf name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">neighbor</span> - Specify a neighbor router. Required only for non-multicast networks. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">id</span> - Neighbor entry id. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">ip</span> - IP address. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">network</span> - Enable RIP routing on an IP network. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">id</span> - Network entry id. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">prefix</span> - Network prefix. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">offset_list</span> - Offset list to modify RIP metric. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">access_list</span> - Access list name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">direction</span> - Offset list direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
                <li> <span class="li-head">id</span> - Offset-list id. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">interface</span> - Interface to match. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">offset</span> - Metric value. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                </ul>
            <li> <span class="li-head">passive_interface</span> - Passive interface configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">name</span> - Passive interface name. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">recv_buffer_size</span> - receiving buffer size <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">redistribute</span> - Redistribute configuration. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">flags</span> - flags <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">metric</span> - Redistribute metric setting. <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">name</span> - Redistribute name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">routemap</span> - Route map name. <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">status</span> - status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
                </ul>
            <li> <span class="li-head">timeout_timer</span> - Routing information timeout timer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">update_timer</span> - Routing table update timer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">version</span> - RIP version <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
            </ul>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: RIP configuration.
      fortinet.fortiswitch.fortiswitch_router_rip:
          router_rip:
              bfd: "enable"
              default_information_originate: "enable"
              default_metric: "5"
              distance:
                  -
                      access_list: "<your_own_value> (source router.access-list.name)"
                      distance: "8"
                      id: "9"
                      prefix: "<your_own_value>"
              distribute_list:
                  -
                      direction: "in"
                      id: "13"
                      interface: "<your_own_value> (source system.interface.name)"
                      listname: "<your_own_value> (source router.access-list.name router.prefix-list.name)"
                      status: "enable"
              garbage_timer: "17"
              interface:
                  -
                      auth_keychain: "<your_own_value> (source router.key-chain.name)"
                      auth_mode: "none"
                      auth_string: "<your_own_value>"
                      bfd: "enable"
                      flags: "23"
                      name: "default_name_24 (source system.interface.name)"
                      receive_version: "global"
                      send_version: "global"
                      send_version2_broadcast: "disable"
                      split_horizon: "poisoned"
                      split_horizon_status: "enable"
              name: "default_name_30"
              neighbor:
                  -
                      id: "32"
                      ip: "<your_own_value>"
              network:
                  -
                      id: "35"
                      prefix: "<your_own_value>"
              offset_list:
                  -
                      access_list: "<your_own_value> (source router.access-list.name)"
                      direction: "in"
                      id: "40"
                      interface: "<your_own_value> (source system.interface.name)"
                      offset: "42"
                      status: "enable"
              passive_interface:
                  -
                      name: "default_name_45 (source system.interface.name)"
              recv_buffer_size: "1073741823"
              redistribute:
                  -
                      flags: "48"
                      metric: "49"
                      name: "default_name_50"
                      routemap: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
              timeout_timer: "53"
              update_timer: "54"
              version: "1"
              vrf:
                  -
                      default_information_originate: "enable"
                      default_metric: "58"
                      distance:
                          -
                              access_list: "<your_own_value> (source router.access-list.name)"
                              distance: "61"
                              id: "62"
                              prefix: "<your_own_value>"
                      distribute_list:
                          -
                              direction: "in"
                              id: "66"
                              interface: "<your_own_value> (source system.interface.name)"
                              listname: "<your_own_value> (source router.access-list.name router.prefix-list.name)"
                              status: "enable"
                      garbage_timer: "70"
                      interface:
                          -
                              auth_keychain: "<your_own_value> (source router.key-chain.name)"
                              auth_mode: "none"
                              auth_string: "<your_own_value>"
                              flags: "75"
                              name: "default_name_76 (source system.interface.name)"
                              receive_version: "global"
                              send_version: "global"
                              send_version2_broadcast: "disable"
                              split_horizon: "poisoned"
                              split_horizon_status: "enable"
                      name: "default_name_82 (source router.vrf.name)"
                      neighbor:
                          -
                              id: "84"
                              ip: "<your_own_value>"
                      network:
                          -
                              id: "87"
                              prefix: "<your_own_value>"
                      offset_list:
                          -
                              access_list: "<your_own_value> (source router.access-list.name)"
                              direction: "in"
                              id: "92"
                              interface: "<your_own_value> (source system.interface.name)"
                              offset: "94"
                              status: "enable"
                      passive_interface:
                          -
                              name: "default_name_97 (source system.interface.name)"
                      recv_buffer_size: "1073741823"
                      redistribute:
                          -
                              flags: "100"
                              metric: "101"
                              name: "default_name_102"
                              routemap: "<your_own_value> (source router.route-map.name)"
                              status: "enable"
                      timeout_timer: "105"
                      update_timer: "106"
                      version: "1"


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
