:source: fortiswitch_router_route_map.py

:orphan:

.. fortiswitch_router_route_map:

fortiswitch_router_route_map -- Route map configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and route_map category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_route_map</td>
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
    <li> <span class="li-head">router_route_map</span> - Route map configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">comments</span> - Description/comments. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">protocol</span> - Route-map type. <span class="li-normal">type: str</span> <span class="li-normal">choices: ospf, ospf6, rip, bgp, isis, zebra, ripng, isis6</span> </li>
        <li> <span class="li-head">rule</span> - Rule. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">action</span> - Action. <span class="li-normal">type: str</span> <span class="li-normal">choices: permit, deny</span> </li>
            <li> <span class="li-head">id</span> - Rule id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">match_as_path</span> - Match BGP AS path list. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">match_community</span> - Match BGP community list. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">match_community_exact</span> - Do exact matching of communities. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">match_flags</span> - Match-flags. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">match_interface</span> - Match interface configuration. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">match_ip6_address</span> - Match ipv6 address permitted by access-list6 or prefix-list6. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">match_ip_address</span> - Match ip address permitted by access-list or prefix-list. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">match_ip_nexthop</span> - Match next hop ip address passed by access-list or prefix-list. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">match_metric</span> - Match metric for redistribute routes. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">match_origin</span> - Match BGP origin code. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, egp, igp, incomplete</span> </li>
            <li> <span class="li-head">match_route_type</span> - Match route type. <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
            <li> <span class="li-head">match_tag</span> - Match tag. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">set_aggregator_as</span> - Set BGP aggregator AS. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">set_aggregator_ip</span> - Set BGP aggregator IP. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">set_aspath</span> - Prepend BGP AS path attribute. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">as</span> - AS number, value range from 0 to 4294967295 <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">set_atomic_aggregate</span> - BGP atomic aggregate attribute. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">set_community</span> - Set BGP community attribute. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">community</span> - AA|AA:NN|internet|local-AS|no-advertise|no-export. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">set_community_additive</span> - Add set-community to existing community. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">set_community_delete</span> - Delete communities matching community list. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">set_extcommunity_rt</span> - Set Route Target extended community. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">community</span> - AA:NN. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">set_extcommunity_soo</span> - Set Site-of-Origin extended community. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">community</span> - AA:NN. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">set_flags</span> - Set-flags. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">set_ip6_nexthop</span> - Set ipv6 global address of next hop. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">set_ip6_nexthop_local</span> - Set ipv6 local address of next hop. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">set_ip_nexthop</span> - Set ip address of next hop. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">set_local_preference</span> - Set BGP local preference path attribute. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">set_metric</span> - Set the metric value. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">set_metric_type</span> - Set the metric type. <span class="li-normal">type: str</span> <span class="li-normal">choices: 1, 2</span> </li>
            <li> <span class="li-head">set_origin</span> - Set BGP origin code. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, egp, igp, incomplete</span> </li>
            <li> <span class="li-head">set_originator_id</span> - Set BGP originator ID attribute. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">set_tag</span> - Set the tag value. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">set_weight</span> - Set BGP weight for routing table. <span class="li-normal">type: int</span> </li>
            </ul>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Route map configuration.
      fortinet.fortiswitch.fortiswitch_router_route_map:
          state: "present"
          router_route_map:
              comments: "<your_own_value>"
              name: "default_name_4"
              protocol: "ospf"
              rule:
                  -
                      action: "permit"
                      id: "8"
                      match_as_path: "<your_own_value> (source router.aspath-list.name)"
                      match_community: "<your_own_value> (source router.community-list.name)"
                      match_community_exact: "enable"
                      match_flags: "12"
                      match_interface: "<your_own_value> (source system.interface.name)"
                      match_ip6_address: "<your_own_value> (source router.access-list6.name router.prefix-list6.name)"
                      match_ip_address: "<your_own_value> (source router.access-list.name router.prefix-list.name)"
                      match_ip_nexthop: "<your_own_value> (source router.access-list.name router.prefix-list.name)"
                      match_metric: "1073741823"
                      match_origin: "none"
                      match_route_type: "1"
                      match_tag: "1073741823"
                      set_aggregator_as: "2147483647"
                      set_aggregator_ip: "<your_own_value>"
                      set_aspath:
                          -
                              as: "<your_own_value>"
                      set_atomic_aggregate: "enable"
                      set_community:
                          -
                              community: "<your_own_value>"
                      set_community_additive: "enable"
                      set_community_delete: "<your_own_value> (source router.community-list.name)"
                      set_extcommunity_rt:
                          -
                              community: "<your_own_value>"
                      set_extcommunity_soo:
                          -
                              community: "<your_own_value>"
                      set_flags: "34"
                      set_ip6_nexthop: "<your_own_value>"
                      set_ip6_nexthop_local: "<your_own_value>"
                      set_ip_nexthop: "<your_own_value>"
                      set_local_preference: "38"
                      set_metric: "1073741823"
                      set_metric_type: "1"
                      set_origin: "none"
                      set_originator_id: "<your_own_value>"
                      set_tag: "1073741823"
                      set_weight: "1073741823"


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
