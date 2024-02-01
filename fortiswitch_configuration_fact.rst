:source: fortiswitch_configuration_fact.py

:orphan:

.. :

fortiswitch_configuration_fact -- Retrieve Facts of FortiSwitch Configurable Objects.
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.11

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- Collects facts from network devices running the fortiSwitch operating system. This module places the facts gathered in the fact tree keyed by the respective resource name.  This facts module will only collect those facts which user specified in playbook.



Requirements
------------
The below requirements are needed on the host that executes this module.

- install galaxy collection fortinet.fortiswitch  >= ``1.0.0``.


Parameters
----------


.. raw:: html

    <ul>
    <li> <span class="li-head">enable_log</span> - Enable/Disable logging for task. <span class="li-normal">type: bool</span> <span class="li-required">required: False</span> <span class="li-normal">default: False</span> </li>
    <li> <span class="li-head">filters</span> - A list of expressions to filter the returned results. <span class="li-normal">type: list</span> <span class="li-required">required: False</span>
     <a id='label0' href="javascript:ContentClick('label1', 'label0');" onmouseover="ContentPreview('label1');" onmouseout="ContentUnpreview('label1');" title="click to collapse or expand..."> more... </a>
     <div id="label1" style="display:none">
     Filter item must be in the following format: <code class="docutils literal notranslate"><span class="pre">[key][operator][pattern]</span></code>, operators could be found in the table:
     <table border="1">
        <tr>
         <td><code class="docutils literal notranslate">Operator </code></td>
         <td><code class="docutils literal notranslate">Case sensitive </code></td>
         <td><code class="docutils literal notranslate">Description </code></td>
        </tr>
      <tr>
       <td>==</td>
       <td>Yes</td>
       <td>Pattern must be identical to the value.</td>
      </tr>
      <tr>
       <td>=*</td>
       <td>No</td>
       <td>Pattern must be identical to the value.</td>
      </tr>
      <tr>
       <td>!=</td>
       <td>Yes</td>
       <td>Pattern does not match the value.</td>
      </tr>
      <tr>
       <td>!*</td>
       <td>No</td>
       <td>Pattern does not match the value.</td>
      </tr>
      <tr>
       <td>=@</td>
       <td>No</td>
       <td>Pattern found within value.</td>
      </tr>
      <tr>
       <td>!@</td>
       <td>No</td>
       <td>Pattern not found within value.</td>
      </tr>
      <tr>
       <td><=</td>
       <td>n/a</td>
       <td>Value must be less than or equal to pattern.</td>
      </tr>
      <tr>
       <td><</td>
       <td>n/a</td>
       <td>Value must be less than pattern.</td>
      </tr>
      <tr>
       <td>>=</td>
       <td>n/a</td>
       <td>Value must be greater than or equal to pattern.</td>
      </tr>
      <tr>
       <td>></td>
       <td>n/a</td>
       <td>Value must be greater than pattern.</td>
      </tr>
      </table>
     </div>
    </li>
    <li> <span class="li-head">sorters</span> - A list of expressions to sort the returned results. <span class="li-normal">type: list</span> <span class="li-required">required: False</span>
        <a id='label2' href="javascript:ContentClick('label3', 'label2');" onmouseover="ContentPreview('label3');" onmouseout="ContentUnpreview('label3');" title="click to collapse or expand..."> more... </a>
       <div id="label3" style="display:none">
       Sorter item must be a <code class="docutils literal notranslate"><span class="pre">[key]</span></code> followed by a <code class="docutils literal notranslate"><span class="pre">,asc</span></code> or <code class="docutils literal notranslate"><span class="pre">,dsc</span></code> order derective.
       <br>
       examples: <code class="docutils literal notranslate"><span class="pre">name,asc</span></code> to sort the result by name in ascending order; <code class="docutils literal notranslate"><span class="pre">vlanid,asc</span></code> to sort the result by vlanid in descending order.
       </div>
    </li>
    <li> <span class="li-head">formatters</span> - A list of fields to display for returned results. <span class="li-normal">type: list</span> <span class="li-required">required: False</span> </li>
    <li><span class="li-head">selector</span> - selector of the retrieved fortimanager facts <span class="li-normal">type: str</span> <span class="li-required">choices:</span></li>
        <li style="list-style: none;"><section class="accordion">
        <input type="checkbox" name="collapse" id="handle2">
        <h2 class="handle">
            <label for="handle2"><u>Show full selector list...</u></label>
        </h2>
        <div class="content">
        <ul class="ul-self">
        <li><span class="li-normal">alertemail_setting</span> </li>
        <li><span class="li-normal">gui_console</span> </li>
        <li><span class="li-normal">log.disk_filter</span> </li>
        <li><span class="li-normal">log.disk_setting</span> </li>
        <li><span class="li-normal">log.fortianalyzer2_filter</span> </li>
        <li><span class="li-normal">log.fortianalyzer2_setting</span> </li>
        <li><span class="li-normal">log.fortianalyzer3_filter</span> </li>
        <li><span class="li-normal">log.fortianalyzer3_setting</span> </li>
        <li><span class="li-normal">log.fortianalyzer_filter</span> </li>
        <li><span class="li-normal">log.fortianalyzer_override-filter</span> </li>
        <li><span class="li-normal">log.fortianalyzer_override-setting</span> </li>
        <li><span class="li-normal">log.fortianalyzer_setting</span> </li>
        <li><span class="li-normal">log.fortiguard_setting</span> </li>
        <li><span class="li-normal">log.memory_filter</span> </li>
        <li><span class="li-normal">log.memory_global-setting</span> </li>
        <li><span class="li-normal">log.memory_setting</span> </li>
        <li><span class="li-normal">log.remote_setting</span> </li>
        <li><span class="li-normal">log.syslogd2_filter</span> </li>
        <li><span class="li-normal">log.syslogd2_setting</span> </li>
        <li><span class="li-normal">log.syslogd3_filter</span> </li>
        <li><span class="li-normal">log.syslogd3_setting</span> </li>
        <li><span class="li-normal">log.syslogd_filter</span> </li>
        <li><span class="li-normal">log.syslogd_override-filter</span> </li>
        <li><span class="li-normal">log.syslogd_override-setting</span> </li>
        <li><span class="li-normal">log.syslogd_setting</span> </li>
        <li><span class="li-normal">log_custom-field</span>  <span class="li-required">param: id</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">log_eventfilter</span> </li>
        <li><span class="li-normal">log_gui</span> </li>
        <li><span class="li-normal">router_access-list</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_access-list6</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_aspath-list</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_auth-path</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_bgp</span> </li>
        <li><span class="li-normal">router_community-list</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_gwdetect</span>  <span class="li-required">param: interface</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_isis</span> </li>
        <li><span class="li-normal">router_key-chain</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_multicast</span> </li>
        <li><span class="li-normal">router_multicast-flow</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_ospf</span> </li>
        <li><span class="li-normal">router_ospf6</span> </li>
        <li><span class="li-normal">router_policy</span>  <span class="li-required">param: seq-num</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_prefix-list</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_prefix-list6</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_rip</span> </li>
        <li><span class="li-normal">router_ripng</span> </li>
        <li><span class="li-normal">router_route-map</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_setting</span> </li>
        <li><span class="li-normal">router_static</span>  <span class="li-required">param: seq-num</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_static6</span>  <span class="li-required">param: seq-num</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">router_vrf</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch-controller_global</span> </li>
        <li><span class="li-normal">switch.acl.service_custom</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.acl_802-1X</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.acl_egress</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.acl_ingress</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.acl_policer</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.acl_prelookup</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.acl_settings</span> </li>
        <li><span class="li-normal">switch.igmp-snooping_globals</span> </li>
        <li><span class="li-normal">switch.lldp_profile</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.lldp_settings</span> </li>
        <li><span class="li-normal">switch.macsec_profile</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.mld-snooping_globals</span> </li>
        <li><span class="li-normal">switch.network-monitor_directed</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.network-monitor_settings</span> </li>
        <li><span class="li-normal">switch.ptp_policy</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.ptp_settings</span> </li>
        <li><span class="li-normal">switch.qos_dot1p-map</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.qos_ip-dscp-map</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.qos_qos-policy</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.stp_instance</span>  <span class="li-required">param: id</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch.stp_settings</span> </li>
        <li><span class="li-normal">switch_auto-isl-port-group</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_auto-network</span> </li>
        <li><span class="li-normal">switch_domain</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_global</span> </li>
        <li><span class="li-normal">switch_interface</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_ip-mac-binding</span>  <span class="li-required">param: seq-num</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_mirror</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_phy-mode</span> </li>
        <li><span class="li-normal">switch_physical-port</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_quarantine</span>  <span class="li-required">param: mac</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_raguard-policy</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_security-feature</span> </li>
        <li><span class="li-normal">switch_static-mac</span>  <span class="li-required">param: seq-num</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_storm-control</span> </li>
        <li><span class="li-normal">switch_trunk</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_virtual-wire</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_vlan</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">switch_vlan-tpid</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.alias_command</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.alias_group</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.autoupdate_clientoverride</span> </li>
        <li><span class="li-normal">system.autoupdate_override</span> </li>
        <li><span class="li-normal">system.autoupdate_push-update</span> </li>
        <li><span class="li-normal">system.autoupdate_schedule</span> </li>
        <li><span class="li-normal">system.autoupdate_tunneling</span> </li>
        <li><span class="li-normal">system.certificate_ca</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.certificate_crl</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.certificate_local</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.certificate_ocsp</span> </li>
        <li><span class="li-normal">system.certificate_remote</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.dhcp_server</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.ptp_interface-policy</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.ptp_profile</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.schedule_group</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.schedule_onetime</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.schedule_recurring</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.snmp_community</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system.snmp_sysinfo</span> </li>
        <li><span class="li-normal">system.snmp_user</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_accprofile</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_admin</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_alarm</span> </li>
        <li><span class="li-normal">system_alertemail</span> </li>
        <li><span class="li-normal">system_arp-table</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_auto-script</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_automation-action</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_automation-destination</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_automation-stitch</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_automation-trigger</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_bug-report</span> </li>
        <li><span class="li-normal">system_central-management</span> </li>
        <li><span class="li-normal">system_console</span> </li>
        <li><span class="li-normal">system_dns</span> </li>
        <li><span class="li-normal">system_dns-database</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_dns-server</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_email-server</span> </li>
        <li><span class="li-normal">system_flan-cloud</span> </li>
        <li><span class="li-normal">system_flow-export</span> </li>
        <li><span class="li-normal">system_fm</span> </li>
        <li><span class="li-normal">system_fortianalyzer</span> </li>
        <li><span class="li-normal">system_fortianalyzer2</span> </li>
        <li><span class="li-normal">system_fortianalyzer3</span> </li>
        <li><span class="li-normal">system_fortiguard</span> </li>
        <li><span class="li-normal">system_fortiguard-log</span> </li>
        <li><span class="li-normal">system_fortimanager</span> </li>
        <li><span class="li-normal">system_fsw-cloud</span> </li>
        <li><span class="li-normal">system_global</span> </li>
        <li><span class="li-normal">system_interface</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_ipv6-neighbor-cache</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_link-monitor</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_location</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_mac-address-table</span>  <span class="li-required">param: mac</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_management-tunnel</span> </li>
        <li><span class="li-normal">system_ntp</span> </li>
        <li><span class="li-normal">system_object-tag</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_password-policy</span> </li>
        <li><span class="li-normal">system_port-pair</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_proxy-arp</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_resource-limits</span> </li>
        <li><span class="li-normal">system_session-ttl</span> </li>
        <li><span class="li-normal">system_settings</span> </li>
        <li><span class="li-normal">system_sflow</span> </li>
        <li><span class="li-normal">system_sniffer-profile</span>  <span class="li-required">param: profile-name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_tos-based-priority</span>  <span class="li-required">param: id</span>  <span class="li-required">type: int</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_vdom</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_vdom-dns</span> </li>
        <li><span class="li-normal">system_vdom-property</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_vxlan</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">system_web</span> </li>
        <li><span class="li-normal">system_zone</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">user_group</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">user_ldap</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">user_local</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">user_peer</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">user_peergrp</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">user_radius</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        <li><span class="li-normal">user_setting</span> </li>
        <li><span class="li-normal">user_tacacs+</span>  <span class="li-required">param: name</span>  <span class="li-required">type: str</span> <span class="li-required">required: True </span></li>
        </ul>
        </div>
        </section>
    <li><span class="li-head">params</span> - the parameter for each selector, see definition in above list.<span class="li-normal">type: dict</span></li>
    <li><span class="li-head">selectors</span> - selectors list allows to pass more than one selector and its parameters in a task.<span class="li-normal">type: list</span></li>

Notes
-----

.. note::

   - Different ``selector`` may have different parameters, users are expected to look up them for a specific selector.

   - For some selectors, the objects are global, no ``params`` are allowed to appear.

   - If ``params`` is empty a non-unique object, the whole object list is returned.

   - This module has support for all configuration API, excluding any monitor API.

   - The result of API request is stored in ``results`` as a list.

   - There are three filtering parameters: ``filters``, ``sorters`` and ``formatters``, please see `filtering spec`_ for more information.


Examples
--------

.. code-block:: yaml+jinja

    - hosts: fortiswitch01
      connection: httpapi
      collections:
        - fortinet.fortiswitch
      vars:
        ansible_httpapi_use_ssl: true
        ansible_httpapi_validate_certs: false
        ansible_httpapi_port: 443
      tasks:
      - name: Get multiple selectors info concurrently
        fortiswitch_configuration_fact:
            selectors:
              - selector: system_interface
                params:
                  name: "internal"
              - selector: log_eventfilter

      - name: fact gathering with filters
        fortiswitch_configuration_fact:
            filters:
             - name==internal
            sorters:
             - name,vlanid
            formatters:
             - name
             - vlanid
             selectors:
             - selector: system_interface

Return Values
-------------
Common return values are documented: https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#common-return-values, the following are the fields unique to this module:

.. raw:: html

    <ul>

    <li> <span class="li-return">build</span> - Build number of the fortiswitch image <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 1547</span></li>
    <li> <span class="li-return">http_method</span> - Last method used to provision the content into FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: GET</span></li>
    <li> <span class="li-return">name</span> - Name of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: firmware</span></li>
    <li> <span class="li-return">path</span> - Path of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: system</span></li>
    <li> <span class="li-return">results</span> - Object list retrieved from device. <span class="li-normal">returned: always</span> <span class="li-normal">type: list</span></li>
    <li> <span class="li-return">revision</span> - Internal revision number <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 17.0.2.10658</span></li>
    <li> <span class="li-return">serial</span> - Serial number of the unit <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: FGVMEVYYQT3AB5352</span></li>
    <li> <span class="li-return">status</span> - Indication of the operation's result <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: success</span></li>
    <li> <span class="li-return">version</span> - Version of the FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: v5.6.3</span></li>
    <li> <span class="li-return">ansible_facts</span> - The list of fact subsets collected from the device <span class="li-normal">returned: always</span> <span class="li-normal">type: dict</span></li>
    </ul>

Status
------

- This module is not guaranteed to have a backwards compatible interface.


Authors
-------

- Link Zheng (@chillancezen)
- Jie Xue (@JieX19)
- Hongbin Lu (@fgtdev-hblu)
- Frank Shen (@fshen01)


.. hint::
    If you notice any issues in this documentation, you can create a pull request to improve it.

.. _filtering spec: https://fndn.fortinet.net/index.php?/fortiapi/1-fortios/597/
