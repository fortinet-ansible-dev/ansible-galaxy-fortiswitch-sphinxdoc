:source: fortiswitch_router_ripng.py

:orphan:

.. fortiswitch_router_ripng:

fortiswitch_router_ripng -- router ripng configuratio in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and ripng category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_ripng</td>
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
    <li> <span class="li-head">router_ripng</span> - router ripng configuration <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">aggregate_address</span> - Set aggregate RIPng route announcement. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Aggregate-address entry id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix6</span> - Aggregate-address prefix. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">bfd</span> - Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">default_information_originate</span> - Generate a default route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">default_metric</span> - Default metric of redistribute routes (Except connected). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distribute_list</span> - Filter networks in routing updates. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">direction</span> - Distribute list direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
            <li> <span class="li-head">id</span> - Distribute-list id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Distribute list interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">listname</span> - Distribute access/prefix list name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">garbage_timer</span> - Garbage collection timer. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">interface</span> - RIPng interface configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">flags</span> - Flags. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - Interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">passive</span> - Suppress routing updates on an interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">split_horizon</span> - Split horizon type. <span class="li-normal">type: str</span> <span class="li-normal">choices: poisoned, regular</span> </li>
            <li> <span class="li-head">split_horizon_status</span> - Enable/disable split horizon. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">offset_list</span> - Offset list to modify RIPng metric. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">access_list6</span> - Ipv6 access list name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">direction</span> - Offset list direction. <span class="li-normal">type: str</span> <span class="li-normal">choices: in, out</span> </li>
            <li> <span class="li-head">id</span> - Offset-list id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Interface name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">offset</span> - Metric offset. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">status</span> - Status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">redistribute</span> - Redistribute configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">flags</span> - Flags <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">metric</span> - Redistribute metric setting. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - Redistribute name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">routemap</span> - Route map name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">timeout_timer</span> - Routing information timeout timer. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">update_timer</span> - Routing table update timer. <span class="li-normal">type: int</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: router ripng configuration
      fortinet.fortiswitch.fortiswitch_router_ripng:
          router_ripng:
              aggregate_address:
                  -
                      id: "4"
                      prefix6: "<your_own_value>"
              bfd: "enable"
              default_information_originate: "enable"
              default_metric: "8"
              distribute_list:
                  -
                      direction: "in"
                      id: "11"
                      interface: "<your_own_value> (source system.interface.name)"
                      listname: "<your_own_value> (source router.access-list6.name router.prefix-list6.name)"
                      status: "enable"
              garbage_timer: "15"
              interface:
                  -
                      flags: "17"
                      name: "default_name_18 (source system.interface.name)"
                      passive: "enable"
                      split_horizon: "poisoned"
                      split_horizon_status: "enable"
              offset_list:
                  -
                      access_list6: "<your_own_value> (source router.access-list6.name)"
                      direction: "in"
                      id: "25"
                      interface: "<your_own_value> (source system.interface.name)"
                      offset: "27"
                      status: "enable"
              redistribute:
                  -
                      flags: "30"
                      metric: "31"
                      name: "default_name_32"
                      routemap: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
              timeout_timer: "35"
              update_timer: "36"


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
