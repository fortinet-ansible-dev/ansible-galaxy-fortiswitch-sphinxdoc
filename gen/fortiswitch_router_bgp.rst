:source: fortiswitch_router_bgp.py

:orphan:

.. fortiswitch_router_bgp:

fortiswitch_router_bgp -- BGP configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and bgp category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_bgp</td>
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
    <li> <span class="li-head">router_bgp</span> - BGP configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">admin_distance</span> - Administrative distance modifications. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">distance</span> - Administrative distance to apply (1 - 255). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">neighbour_prefix</span> - Neighbor address prefix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_list</span> - Access list of routes to apply new distance to. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">admin_distance6</span> - Administrative distance modifications. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">distance</span> - Administrative distance to apply (1 - 255). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">neighbour_prefix6</span> - Neighbor IPV6 prefix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route6_list</span> - Access list of routes to apply new distance to. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">aggregate_address</span> - BGP aggregate address table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">as_set</span> - Enable/disable generate AS set path information. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix</span> - Aggregate prefix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">summary_only</span> - Enable/disable filter more specific routes from updates. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">aggregate_address6</span> - BGP IPv6 aggregate address table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix6</span> - Aggregate IPv6 prefix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">summary_only</span> - Enable/disable filter more specific routes from updates. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">always_compare_med</span> - Enable/disable always compare MED. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">as</span> - Router AS number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">bestpath_as_path_ignore</span> - Enable/disable ignore AS path. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bestpath_aspath_multipath_relax</span> - Allow load sharing across routes that have different AS paths (but same length). <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">bestpath_cmp_confed_aspath</span> - Enable/disable compare federation AS path length. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bestpath_cmp_routerid</span> - Enable/disable compare router ID for identical EBGP paths. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bestpath_med_confed</span> - Enable/disable compare MED among confederation paths. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">bestpath_med_missing_as_worst</span> - Enable/disable treat missing MED as least preferred. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">client_to_client_reflection</span> - Enable/disable client-to-client route reflection. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">cluster_id</span> - Route reflector cluster ID. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">confederation_identifier</span> - Confederation identifier. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">confederation_peers</span> - Confederation peers. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">peer</span> - Peer ID. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">dampening</span> - Enable/disable route-flap dampening. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">dampening_max_suppress_time</span> - Maximum minutes a route can be suppressed. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dampening_reachability_half_life</span> - Reachability half-life time for penalty (minutes). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dampening_reuse</span> - Threshold to unsuppress routes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dampening_suppress</span> - Threshold to suppress routes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">default_local_preference</span> - Default local preference. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">deterministic_med</span> - Enable/disable enforce deterministic comparison of MED. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">distance_external</span> - Distance for routes external to the AS. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distance_internal</span> - Distance for routes internal to the AS. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">distance_local</span> - Distance for routes local to the AS. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ebgp_requires_policy</span> - Enable/disable require in and out policy for eBGP peers (RFC8212). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">enforce_first_as</span> - Enable/disable enforce first AS for EBGP routes. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">fast_external_failover</span> - Enable/disable reset peer BGP session if link goes down. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">graceful_stalepath_time</span> - Time to hold stale paths of restarting neighbour(sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">holdtime_timer</span> - Number of seconds to mark peer as dead. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">keepalive_timer</span> - Frequency to send keepalive requests. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">log_neighbour_changes</span> - Enable logging of BGP neighbour"s changes <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">maximum_paths_ebgp</span> - Maximum paths for ebgp ecmp. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">maximum_paths_ibgp</span> - Maximum paths for ibgp ecmp. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">neighbor</span> - BGP neighbor table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">activate</span> - Enable/disable address family IPv4 for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">activate6</span> - Enable/disable address family IPv6 for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">activate_evpn</span> - Enable/disable address family evpn for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">advertisement_interval</span> - Minimum interval (seconds) between sending updates. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">allowas_in</span> - IPv4 The maximum number of occurrence of my AS number allowed. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">allowas_in6</span> - IPv6 The maximum number of occurrence of my AS number allowed. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">allowas_in_enable</span> - Enable/disable IPv4 Enable to allow my AS in AS path. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">allowas_in_enable6</span> - Enable/disable IPv6 Enable to allow my AS in AS path. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">allowas_in_enable_evpn</span> - Enable/disable EVPN Enable to allow my AS in AS path. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">as_override</span> - Enable/disable replace peer AS with own AS for IPv4. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">as_override6</span> - Enable/disable replace peer AS with own AS for IPv6. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">attribute_unchanged</span> - IPv4 List of attributes that should be unchanged. <span class="li-normal">type: str</span> <span class="li-normal">choices: as-path, med, next-hop</span> </li>
            <li> <span class="li-head">attribute_unchanged6</span> - IPv6 List of attributes that should be unchanged. <span class="li-normal">type: str</span> <span class="li-normal">choices: as-path, med, next-hop</span> </li>
            <li> <span class="li-head">attribute_unchanged_evpn</span> - EVPN List of attributes that should be unchanged. <span class="li-normal">type: str</span> <span class="li-normal">choices: as-path, med</span> </li>
            <li> <span class="li-head">bfd</span> - Enable/disable BFD for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">bfd_session_mode</span> - Single or multihop BFD session to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: automatic, multihop, singlehop</span> </li>
            <li> <span class="li-head">capability_default_originate</span> - Enable/disable advertise default IPv4 route to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_default_originate6</span> - Enable/disable advertise default IPv6 route to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_dynamic</span> - Enable/disable advertise dynamic capability to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_extended_nexthop</span> - Enable/disable extended nexthop capability. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_orf</span> - Accept/Send IPv4 ORF lists to/from this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, receive, send, both</span> </li>
            <li> <span class="li-head">capability_orf6</span> - Accept/Send IPv6 ORF lists to/from this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, receive, send, both</span> </li>
            <li> <span class="li-head">connect_timer</span> - Interval (seconds) for connect timer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">default_originate_routemap</span> - Route map to specify criteria to originate IPv4 default. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">default_originate_routemap6</span> - Route map to specify criteria to originate IPv6 default. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_in</span> - Filter for IPv4 updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_in6</span> - Filter for IPv6 updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_out</span> - Filter for IPv4 updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_out6</span> - Filter for IPv6 updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">dont_capability_negotiate</span> - Don"t negotiate capabilities with this neighbor <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ebgp_enforce_multihop</span> - Enable/disable allow multi-hop next-hops from EBGP neighbors. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ebgp_multihop_ttl</span> - EBGP multihop TTL for this peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ebgp_ttl_security_hops</span> - Specify the maximum number of hops to the EBGP peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">enforce_first_as</span> - Enable/disable  - Enable to enforce first AS for all(IPV4/IPV6) EBGP routes. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">filter_list_in</span> - BGP aspath filter for IPv4 inbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">filter_list_in6</span> - BGP filter for IPv6 inbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">filter_list_out</span> - BGP aspath filter for IPv4 outbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">filter_list_out6</span> - BGP filter for IPv6 outbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">holdtime_timer</span> - Interval (seconds) before peer considered dead. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Interface. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ip</span> - IP/IPv6 address of neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">keep_alive_timer</span> - Keepalive timer interval (seconds). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix</span> - Maximum number of IPv4 prefixes to accept from this peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix6</span> - Maximum number of IPv6 prefixes to accept from this peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix_threshold</span> - Maximum IPv4 prefix threshold value (1-100 percent). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix_threshold6</span> - Maximum IPv6 prefix threshold value (1-100 percent) <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix_warning_only</span> - Enable/disable IPv4 Only give warning message when threshold is exceeded. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">maximum_prefix_warning_only6</span> - Enable/disable IPv6 Only give warning message when threshold is exceeded. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">next_hop_self</span> - Enable/disable IPv4 next-hop calculation for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">next_hop_self6</span> - Enable/disable IPv6 next-hop calculation for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">override_capability</span> - Enable/disable override result of capability negotiation. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">passive</span> - Enable/disable sending of open messages to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">password</span> - Password used in MD5 authentication. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_in</span> - IPv4 Inbound filter for updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_in6</span> - IPv6 Inbound filter for updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_out</span> - IPv4 Outbound filter for updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_out6</span> - IPv6 Outbound filter for updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">remote_as</span> - AS number of neighbor. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">remove_private_as</span> - Enable/disable remove private AS number from IPv4 outbound updates. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">remove_private_as6</span> - Enable/disable remove private AS number from IPv6 outbound updates. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_map_in</span> - IPv4 Inbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_in6</span> - IPv6 Inbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_in_evpn</span> - EVPN Inbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_out</span> - IPv4 outbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_out6</span> - IPv6 Outbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_out_evpn</span> - EVPN outbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_reflector_client</span> - Enable/disable IPv4 AS route reflector client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_reflector_client6</span> - Enable/disable IPv6 AS route reflector client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_reflector_client_evpn</span> - Enable/disable EVPN AS route reflector client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_server_client</span> - Enable/disable IPv4 AS route server client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_server_client6</span> - Enable/disable IPv6 AS route server client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">send_community</span> - IPv4 Send community attribute to neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: standard, extended, both, disable</span> </li>
            <li> <span class="li-head">send_community6</span> - IPv6 Send community attribute to neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: standard, extended, both, disable</span> </li>
            <li> <span class="li-head">shutdown</span> - Enable/disable shutdown this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">soft_reconfiguration</span> - Enable/disable allow IPv4 inbound soft reconfiguration. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">soft_reconfiguration6</span> - Enable/disable allow IPv6 inbound soft reconfiguration. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">soft_reconfiguration_evpn</span> - Enable/disable allow EVPN inbound soft reconfiguration. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">strict_capability_match</span> - Enable/disable strict capability matching. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">unsuppress_map</span> - IPv4 Route map to selectively unsuppress suppressed routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">unsuppress_map6</span> - IPv6 Route map to selectively unsuppress suppressed routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">update_source</span> - Interface to use as source IP/IPv6 address of TCP connections. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">weight</span> - Neighbor weight. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">neighbor_group</span> - BGP neighbor group table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">activate</span> - Enable/disable address family IPv4 for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">activate6</span> - Enable/disable address family IPv6 for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">activate_evpn</span> - Enable/disable address family evpn for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">advertisement_interval</span> - Minimum interval (seconds) between sending updates. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">allowas_in</span> - IPv4 The maximum number of occurrence of my AS number allowed. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">allowas_in6</span> - IPv6 The maximum number of occurrence of my AS number allowed. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">allowas_in_enable</span> - Enable/disable IPv4 Enable to allow my AS in AS path. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">allowas_in_enable6</span> - Enable/disable IPv6 - Enable to allow my AS in AS path. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">allowas_in_enable_evpn</span> - Enable/disable EVPN Enable to allow my AS in AS path. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">as_override</span> - Enable/disable replace peer AS with own AS for IPv4. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">as_override6</span> - Enable/disable replace peer AS with own AS for IPv6. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">attribute_unchanged</span> - IPv4 List of attributes that should be unchanged. <span class="li-normal">type: str</span> <span class="li-normal">choices: as-path, med, next-hop</span> </li>
            <li> <span class="li-head">attribute_unchanged6</span> - IPv6 List of attributes that should be unchanged. <span class="li-normal">type: str</span> <span class="li-normal">choices: as-path, med, next-hop</span> </li>
            <li> <span class="li-head">attribute_unchanged_evpn</span> - EVPN List of attributes that should be unchanged. <span class="li-normal">type: str</span> <span class="li-normal">choices: as-path, med</span> </li>
            <li> <span class="li-head">bfd</span> - Enable/disable BFD for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_default_originate</span> - Enable/disable advertise default IPv4 route to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_default_originate6</span> - Enable/disable advertise default IPv6 route to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_dynamic</span> - Enable/disable advertise dynamic capability to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_extended_nexthop</span> - Enable/disable extended nexthop capability. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">capability_orf</span> - Accept/Send IPv4 ORF lists to/from this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, receive, send, both</span> </li>
            <li> <span class="li-head">capability_orf6</span> - Accept/Send IPv6 ORF lists to/from this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, receive, send, both</span> </li>
            <li> <span class="li-head">connect_timer</span> - Interval (seconds) for connect timer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">default_originate_routemap</span> - Route map to specify criteria to originate IPv4 default. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">default_originate_routemap6</span> - Route map to specify criteria to originate IPv6 default. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_in</span> - Filter for IPv4 updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_in6</span> - Filter for IPv6 updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_out</span> - Filter for IPv4 updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">distribute_list_out6</span> - Filter for IPv6 updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">dont_capability_negotiate</span> - Don"t negotiate capabilities with this neighbor <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ebgp_enforce_multihop</span> - Enable/disable allow multi-hop next-hops from EBGP neighbors. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">ebgp_multihop_ttl</span> - EBGP multihop TTL for this peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">ebgp_ttl_security_hops</span> - Specify the maximum number of hops to the EBGP peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">enforce_first_as</span> - Enable/disable  - Enable to enforce first AS for all(IPV4/IPV6) EBGP routes. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">filter_list_in</span> - BGP aspath filter for IPv4 inbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">filter_list_in6</span> - BGP filter for IPv6 inbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">filter_list_out</span> - BGP aspath filter for IPv4 outbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">filter_list_out6</span> - BGP filter for IPv6 outbound routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">holdtime_timer</span> - Interval (seconds) before peer considered dead. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">interface</span> - Interface(s). <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">interface_name</span> - RVI interface name(s). <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">keep_alive_timer</span> - Keepalive timer interval (seconds). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix</span> - Maximum number of IPv4 prefixes to accept from this peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix6</span> - Maximum number of IPv6 prefixes to accept from this peer. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix_threshold</span> - Maximum IPv4 prefix threshold value (1-100 percent). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix_threshold6</span> - Maximum IPv6 prefix threshold value (1-100 percent) <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">maximum_prefix_warning_only</span> - Enable/disable IPv4 Only give warning message when threshold is exceeded. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">maximum_prefix_warning_only6</span> - Enable/disable IPv6 Only give warning message when threshold is exceeded. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">name</span> - Neighbor group name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">next_hop_self</span> - Enable/disable IPv4 next-hop calculation for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">next_hop_self6</span> - Enable/disable IPv6 next-hop calculation for this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">override_capability</span> - Enable/disable override result of capability negotiation. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">passive</span> - Enable/disable sending of open messages to this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">password</span> - Password used in MD5 authentication. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_in</span> - IPv4 Inbound filter for updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_in6</span> - IPv6 Inbound filter for updates from this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_out</span> - IPv4 Outbound filter for updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">prefix_list_out6</span> - IPv6 Outbound filter for updates to this neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">remote_as</span> - AS number of neighbor. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">remove_private_as</span> - Enable/disable remove private AS number from IPv4 outbound updates. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">remove_private_as6</span> - Enable/disable remove private AS number from IPv6 outbound updates. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_map_in</span> - IPv4 Inbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_in6</span> - IPv6 Inbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_in_evpn</span> - EVPN Inbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_out</span> - IPv4 outbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_out6</span> - IPv6 Outbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map_out_evpn</span> - EVPN outbound route map filter. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_reflector_client</span> - Enable/disable IPv4 AS route reflector client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_reflector_client6</span> - Enable/disable IPv6 AS route reflector client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_reflector_client_evpn</span> - Enable/disable EVPN AS route reflector client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_server_client</span> - Enable/disable IPv4 AS route server client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">route_server_client6</span> - Enable/disable IPv6 AS route server client. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">send_community</span> - IPv4 Send community attribute to neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: standard, extended, both, disable</span> </li>
            <li> <span class="li-head">send_community6</span> - IPv6 Send community attribute to neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: standard, extended, both, disable</span> </li>
            <li> <span class="li-head">shutdown</span> - Enable/disable shutdown this neighbor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">soft_reconfiguration</span> - Enable/disable allow IPv4 inbound soft reconfiguration. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">soft_reconfiguration6</span> - Enable/disable allow IPv6 inbound soft reconfiguration. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">soft_reconfiguration_evpn</span> - Enable/disable allow EVPN inbound soft reconfiguration. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">strict_capability_match</span> - Enable/disable strict capability matching. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">unsuppress_map</span> - IPv4 Route map to selectively unsuppress suppressed routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">unsuppress_map6</span> - IPv6 Route map to selectively unsuppress suppressed routes. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">update_source</span> - Interface to use as source IP/IPv6 address of TCP connections. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">weight</span> - Neighbor weight. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">network</span> - BGP network table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">backdoor</span> - Enable/disable route as backdoor. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix</span> - Network prefix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map</span> - Route map to modify generated route. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">network6</span> - BGP IPv6 network table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">prefix6</span> - Network IPv6 prefix. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map</span> - Route map to modify generated route. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">redistribute</span> - BGP IPv4 redistribute table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Redistribute protocol name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map</span> - Route map name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - Status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">redistribute6</span> - BGP IPv6 redistribute table. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Distribute list entry name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">route_map</span> - Route map name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - Status <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">route_reflector_allow_outbound_policy</span> - Enable/disable route reflector to apply a route-map to reflected routes. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">router_id</span> - Router ID. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">scan_time</span> - Background scanner interval (seconds). <span class="li-normal">type: int</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: BGP configuration.
      fortinet.fortiswitch.fortiswitch_router_bgp:
          router_bgp:
              admin_distance:
                  -
                      distance: "4"
                      id: "5"
                      neighbour_prefix: "<your_own_value>"
                      route_list: "<your_own_value> (source router.access-list.name)"
              admin_distance6:
                  -
                      distance: "9"
                      id: "10"
                      neighbour_prefix6: "<your_own_value>"
                      route6_list: "<your_own_value> (source router.access-list6.name)"
              aggregate_address:
                  -
                      as_set: "enable"
                      id: "15"
                      prefix: "<your_own_value>"
                      summary_only: "enable"
              aggregate_address6:
                  -
                      id: "19"
                      prefix6: "<your_own_value>"
                      summary_only: "enable"
              always_compare_med: "enable"
              as: "2147483647"
              bestpath_as_path_ignore: "enable"
              bestpath_aspath_multipath_relax: "disable"
              bestpath_cmp_confed_aspath: "enable"
              bestpath_cmp_routerid: "enable"
              bestpath_med_confed: "enable"
              bestpath_med_missing_as_worst: "enable"
              client_to_client_reflection: "enable"
              cluster_id: "<your_own_value>"
              confederation_identifier: "32"
              confederation_peers:
                  -
                      peer: "<your_own_value>"
              dampening: "enable"
              dampening_max_suppress_time: "36"
              dampening_reachability_half_life: "37"
              dampening_reuse: "38"
              dampening_suppress: "39"
              default_local_preference: "40"
              deterministic_med: "enable"
              distance_external: "42"
              distance_internal: "43"
              distance_local: "44"
              ebgp_requires_policy: "enable"
              enforce_first_as: "enable"
              fast_external_failover: "enable"
              graceful_stalepath_time: "48"
              holdtime_timer: "49"
              keepalive_timer: "50"
              log_neighbour_changes: "enable"
              maximum_paths_ebgp: "52"
              maximum_paths_ibgp: "53"
              neighbor:
                  -
                      activate: "enable"
                      activate6: "enable"
                      activate_evpn: "enable"
                      advertisement_interval: "58"
                      allowas_in: "59"
                      allowas_in6: "60"
                      allowas_in_enable: "enable"
                      allowas_in_enable6: "enable"
                      allowas_in_enable_evpn: "enable"
                      as_override: "enable"
                      as_override6: "enable"
                      attribute_unchanged: "as-path"
                      attribute_unchanged6: "as-path"
                      attribute_unchanged_evpn: "as-path"
                      bfd: "enable"
                      bfd_session_mode: "automatic"
                      capability_default_originate: "enable"
                      capability_default_originate6: "enable"
                      capability_dynamic: "enable"
                      capability_extended_nexthop: "enable"
                      capability_orf: "none"
                      capability_orf6: "none"
                      connect_timer: "77"
                      default_originate_routemap: "<your_own_value> (source router.route-map.name)"
                      default_originate_routemap6: "<your_own_value> (source router.route-map.name)"
                      description: "<your_own_value>"
                      distribute_list_in: "<your_own_value> (source router.access-list.name)"
                      distribute_list_in6: "<your_own_value> (source router.access-list6.name)"
                      distribute_list_out: "<your_own_value> (source router.access-list.name)"
                      distribute_list_out6: "<your_own_value> (source router.access-list6.name)"
                      dont_capability_negotiate: "enable"
                      ebgp_enforce_multihop: "enable"
                      ebgp_multihop_ttl: "87"
                      ebgp_ttl_security_hops: "88"
                      enforce_first_as: "enable"
                      filter_list_in: "<your_own_value> (source router.aspath-list.name)"
                      filter_list_in6: "<your_own_value> (source router.aspath-list.name)"
                      filter_list_out: "<your_own_value> (source router.aspath-list.name)"
                      filter_list_out6: "<your_own_value> (source router.aspath-list.name)"
                      holdtime_timer: "94"
                      interface: "<your_own_value> (source system.interface.name)"
                      ip: "<your_own_value>"
                      keep_alive_timer: "97"
                      maximum_prefix: "98"
                      maximum_prefix6: "99"
                      maximum_prefix_threshold: "100"
                      maximum_prefix_threshold6: "101"
                      maximum_prefix_warning_only: "enable"
                      maximum_prefix_warning_only6: "enable"
                      next_hop_self: "enable"
                      next_hop_self6: "enable"
                      override_capability: "enable"
                      passive: "enable"
                      password: "<your_own_value>"
                      prefix_list_in: "<your_own_value> (source router.prefix-list.name)"
                      prefix_list_in6: "<your_own_value> (source router.prefix-list6.name)"
                      prefix_list_out: "<your_own_value> (source router.prefix-list.name)"
                      prefix_list_out6: "<your_own_value> (source router.prefix-list6.name)"
                      remote_as: "2147483647"
                      remove_private_as: "enable"
                      remove_private_as6: "enable"
                      route_map_in: "<your_own_value> (source router.route-map.name)"
                      route_map_in6: "<your_own_value> (source router.route-map.name)"
                      route_map_in_evpn: "<your_own_value> (source router.route-map.name)"
                      route_map_out: "<your_own_value> (source router.route-map.name)"
                      route_map_out6: "<your_own_value> (source router.route-map.name)"
                      route_map_out_evpn: "<your_own_value> (source router.route-map.name)"
                      route_reflector_client: "enable"
                      route_reflector_client6: "enable"
                      route_reflector_client_evpn: "enable"
                      route_server_client: "enable"
                      route_server_client6: "enable"
                      send_community: "standard"
                      send_community6: "standard"
                      shutdown: "enable"
                      soft_reconfiguration: "enable"
                      soft_reconfiguration6: "enable"
                      soft_reconfiguration_evpn: "enable"
                      strict_capability_match: "enable"
                      unsuppress_map: "<your_own_value> (source router.route-map.name)"
                      unsuppress_map6: "<your_own_value> (source router.route-map.name)"
                      update_source: "<your_own_value> (source system.interface.name)"
                      weight: "137"
              neighbor_group:
                  -
                      activate: "enable"
                      activate6: "enable"
                      activate_evpn: "enable"
                      advertisement_interval: "142"
                      allowas_in: "143"
                      allowas_in6: "144"
                      allowas_in_enable: "enable"
                      allowas_in_enable6: "enable"
                      allowas_in_enable_evpn: "enable"
                      as_override: "enable"
                      as_override6: "enable"
                      attribute_unchanged: "as-path"
                      attribute_unchanged6: "as-path"
                      attribute_unchanged_evpn: "as-path"
                      bfd: "enable"
                      capability_default_originate: "enable"
                      capability_default_originate6: "enable"
                      capability_dynamic: "enable"
                      capability_extended_nexthop: "enable"
                      capability_orf: "none"
                      capability_orf6: "none"
                      connect_timer: "160"
                      default_originate_routemap: "<your_own_value> (source router.route-map.name)"
                      default_originate_routemap6: "<your_own_value> (source router.route-map.name)"
                      description: "<your_own_value>"
                      distribute_list_in: "<your_own_value> (source router.access-list.name)"
                      distribute_list_in6: "<your_own_value> (source router.access-list6.name)"
                      distribute_list_out: "<your_own_value> (source router.access-list.name)"
                      distribute_list_out6: "<your_own_value> (source router.access-list6.name)"
                      dont_capability_negotiate: "enable"
                      ebgp_enforce_multihop: "enable"
                      ebgp_multihop_ttl: "170"
                      ebgp_ttl_security_hops: "171"
                      enforce_first_as: "enable"
                      filter_list_in: "<your_own_value> (source router.aspath-list.name)"
                      filter_list_in6: "<your_own_value> (source router.aspath-list.name)"
                      filter_list_out: "<your_own_value> (source router.aspath-list.name)"
                      filter_list_out6: "<your_own_value> (source router.aspath-list.name)"
                      holdtime_timer: "177"
                      interface:
                          -
                              interface_name: "<your_own_value> (source system.interface.name)"
                      keep_alive_timer: "180"
                      maximum_prefix: "181"
                      maximum_prefix6: "182"
                      maximum_prefix_threshold: "183"
                      maximum_prefix_threshold6: "184"
                      maximum_prefix_warning_only: "enable"
                      maximum_prefix_warning_only6: "enable"
                      name: "default_name_187"
                      next_hop_self: "enable"
                      next_hop_self6: "enable"
                      override_capability: "enable"
                      passive: "enable"
                      password: "<your_own_value>"
                      prefix_list_in: "<your_own_value> (source router.prefix-list.name)"
                      prefix_list_in6: "<your_own_value> (source router.prefix-list6.name)"
                      prefix_list_out: "<your_own_value> (source router.prefix-list.name)"
                      prefix_list_out6: "<your_own_value> (source router.prefix-list6.name)"
                      remote_as: "<your_own_value>"
                      remove_private_as: "enable"
                      remove_private_as6: "enable"
                      route_map_in: "<your_own_value> (source router.route-map.name)"
                      route_map_in6: "<your_own_value> (source router.route-map.name)"
                      route_map_in_evpn: "<your_own_value> (source router.route-map.name)"
                      route_map_out: "<your_own_value> (source router.route-map.name)"
                      route_map_out6: "<your_own_value> (source router.route-map.name)"
                      route_map_out_evpn: "<your_own_value> (source router.route-map.name)"
                      route_reflector_client: "enable"
                      route_reflector_client6: "enable"
                      route_reflector_client_evpn: "enable"
                      route_server_client: "enable"
                      route_server_client6: "enable"
                      send_community: "standard"
                      send_community6: "standard"
                      shutdown: "enable"
                      soft_reconfiguration: "enable"
                      soft_reconfiguration6: "enable"
                      soft_reconfiguration_evpn: "enable"
                      strict_capability_match: "enable"
                      unsuppress_map: "<your_own_value> (source router.route-map.name)"
                      unsuppress_map6: "<your_own_value> (source router.route-map.name)"
                      update_source: "<your_own_value> (source system.interface.name)"
                      weight: "221"
              network:
                  -
                      backdoor: "enable"
                      id: "224"
                      prefix: "<your_own_value>"
                      route_map: "<your_own_value> (source router.route-map.name)"
              network6:
                  -
                      id: "228"
                      prefix6: "<your_own_value>"
                      route_map: "<your_own_value> (source router.route-map.name)"
              redistribute:
                  -
                      name: "default_name_232"
                      route_map: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
              redistribute6:
                  -
                      name: "default_name_236"
                      route_map: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
              route_reflector_allow_outbound_policy: "enable"
              router_id: "<your_own_value>"
              scan_time: "241"


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
