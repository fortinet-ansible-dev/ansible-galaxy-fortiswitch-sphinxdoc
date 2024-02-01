:source: fortiswitch_monitor_fact.py

:orphan:

.. :

fortiswitch_monitor_fact -- Retrieve Facts of FortiSwitch Monitor Objects.
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.11

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- Collects monitor facts from network devices running the fortiswitch operating system.  This facts module will only collect those facts which user specified in playbook.



Requirements
------------
The below requirements are needed on the host that executes this module.

- install galaxy collection fortinet.fortiswitch >= ``1.0.0``.


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
    <li><span class="li-head">selector</span> - selector of the retrieved fortiSwitch facts <span class="li-normal">type: str</span> <span class="li-required">choices:</span></li>
        <li style="list-style: none;"><section class="accordion">
        <input type="checkbox" name="collapse" id="handle2">
        <h2 class="handle">
            <label for="handle2"><u>Show full selector list...</u></label>
        </h2>
        <div class="content">
        <ul class="ul-self">
        hardware_cpu
        <li><span class="li-head">hardware_cpu</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        hardware_memory
        <li><span class="li-head">hardware_memory</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        router_routing-table
        <li><span class="li-head">router_routing-table</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_802.1x-status
        <li><span class="li-head">switch_802.1x-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_acl-stats
        <li><span class="li-head">switch_acl-stats</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_acl-stats-egress
        <li><span class="li-head">switch_acl-stats-egress</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_acl-stats-ingress
        <li><span class="li-head">switch_acl-stats-ingress</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_acl-stats-prelookup
        <li><span class="li-head">switch_acl-stats-prelookup</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_acl-usage
        <li><span class="li-head">switch_acl-usage</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_cable-diag
        <li><span class="li-head">switch_cable-diag</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_capabilities
        <li><span class="li-head">switch_capabilities</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_dhcp-snooping-client-db
        <li><span class="li-head">switch_dhcp-snooping-client-db</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_dhcp-snooping-client6-db
        <li><span class="li-head">switch_dhcp-snooping-client6-db</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_dhcp-snooping-db
        <li><span class="li-head">switch_dhcp-snooping-db</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_dhcp-snooping-limit-db-details
        <li><span class="li-head">switch_dhcp-snooping-limit-db-details</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_dhcp-snooping-server-db
        <li><span class="li-head">switch_dhcp-snooping-server-db</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_dhcp-snooping-server6-db
        <li><span class="li-head">switch_dhcp-snooping-server6-db</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_faceplate
        <li><span class="li-head">switch_faceplate</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_flapguard-status
        <li><span class="li-head">switch_flapguard-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_igmp-snooping-group
        <li><span class="li-head">switch_igmp-snooping-group</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_lldp-state
        <li><span class="li-head">switch_lldp-state</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_loop-guard-state
        <li><span class="li-head">switch_loop-guard-state</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_mac-address
        <li><span class="li-head">switch_mac-address</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_mac-address-summary
        <li><span class="li-head">switch_mac-address-summary</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_mclag-icl
        <li><span class="li-head">switch_mclag-icl</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_mclag-list
        <li><span class="li-head">switch_mclag-list</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_modules-detail
        <li><span class="li-head">switch_modules-detail</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_modules-limits
        <li><span class="li-head">switch_modules-limits</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_modules-status
        <li><span class="li-head">switch_modules-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_modules-summary
        <li><span class="li-head">switch_modules-summary</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_network-monitor-l2db
        <li><span class="li-head">switch_network-monitor-l2db</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_network-monitor-l3db
        <li><span class="li-head">switch_network-monitor-l3db</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_poe-status
        <li><span class="li-head">switch_poe-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_poe-summary
        <li><span class="li-head">switch_poe-summary</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_port
        <li><span class="li-head">switch_port</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_port-speed
        <li><span class="li-head">switch_port-speed</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_port-statistics
        <li><span class="li-head">switch_port-statistics</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_qos-stats
        <li><span class="li-head">switch_qos-stats</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_stp-state
        <li><span class="li-head">switch_stp-state</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        switch_trunk-state
        <li><span class="li-head">switch_trunk-state</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_dhcp-lease-list
        <li><span class="li-head">system_dhcp-lease-list</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_fan-status
        <li><span class="li-head">system_fan-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_flash-list
        <li><span class="li-head">system_flash-list</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_flow-export-flows
        <li><span class="li-head">system_flow-export-flows</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_flow-export-statistics
        <li><span class="li-head">system_flow-export-statistics</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_hardware-status
        <li><span class="li-head">system_hardware-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_interface-physical
        <li><span class="li-head">system_interface-physical</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_link-monitor-status
        <li><span class="li-head">system_link-monitor-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_log
        <li><span class="li-head">system_log</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_ntp-status
        <li><span class="li-head">system_ntp-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_pcb-temp
        <li><span class="li-head">system_pcb-temp</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_performance-status
        <li><span class="li-head">system_performance-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_psu-status
        <li><span class="li-head">system_psu-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_resource
        <li><span class="li-head">system_resource</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_sniffer-profile-summary
        <li><span class="li-head">system_sniffer-profile-summary</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_status
        <li><span class="li-head">system_status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        system_upgrade-status
        <li><span class="li-head">system_upgrade-status</span> 
        <ul class="ul-self">
                
            </ul>
        
        </li>
        </ul>
        </div>
        </section>
    <li><span class="li-head">params</span> - the parameter for each selector, see definition in above list.<span class="li-normal">type: dict</span></li>


Notes
-----

.. note::

   - Different ``selector`` may have different parameters, users are expected to look up them for a specific selector.

   - For some selectors, the objects are global, no ``params`` are allowed to appear.

   - Not all parameters are required for a slector.

   - This module is exclusivly for FortiSwitch monitor API.

   - The result of API request is stored in ``results``.

   - There are three filtering parameters: ``filters``, ``sorters`` and ``formatters``, please see `filtering spec`_ for more information.

Examples
--------

.. code-block:: yaml+jinja

 - hosts: fortiswitch01
   connection: httpapi
   collections:
   - fortinet.fortiswitch
   vars:
    ansible_httpapi_use_ssl: yes
    ansible_httpapi_validate_certs: no
    ansible_httpapi_port: 443
   tasks:
   - fortiswitch_monitor_fact:
        enable_log: true
        formatters:
          - model_name
        filters:
          - model_name==FortiSwitch
        selectors:
          - selector: 'system_status'

Return Values
-------------
Common return values are documented: https://docs.ansible.com/ansible/latest/reference_appendices/common_return_values.html#common-return-values, the following are the fields unique to this module:

.. raw:: html

    <ul>

    <li> <span class="li-return">build</span> - Build number of the fortiSwitch image <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: 1547</span></li>
    <li> <span class="li-return">http_method</span> - Last method used to provision the content into FortiSwitch <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: GET</span></li>
    <li> <span class="li-return">name</span> - Name of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: firmware</span></li>
    <li> <span class="li-return">path</span> - Path of the table used to fulfill the request <span class="li-normal">returned: always</span> <span class="li-normal">type: str</span> <span class="li-normal">sample: system</span></li>
    <li> <span class="li-return">results</span> - Object list retrieved from device. <span class="li-normal">returned: always</span> <span class="li-normal">type: list</span></li>
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