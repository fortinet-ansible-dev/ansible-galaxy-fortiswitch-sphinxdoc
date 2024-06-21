:source: fortiswitch_switch_physical_port.py

:orphan:

.. fortiswitch_switch_physical_port:

fortiswitch_switch_physical_port -- Physical port specific configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch feature and physical_port category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_physical_port</td>
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
    <li> <span class="li-head">switch_physical_port</span> - Physical port specific configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">cdp_status</span> - CDP transmit and receive status (LLDP must be enabled in LLDP settings). <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, rx-only, tx-only, tx-rx</span> </li>
        <li> <span class="li-head">description</span> - Description. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dmi_status</span> - DMI status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable, global</span> </li>
        <li> <span class="li-head">eee_tx_idle_time</span> - EEE Transmit idle time (microseconds)(0-2560). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">eee_tx_wake_time</span> - EEE Transmit wake time (microseconds)(0-2560). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">egress_drop_mode</span> - Enable/Disable egress drop. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">energy_efficient_ethernet</span> - Enable / disable energy efficient ethernet. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">flap_duration</span> - Period over which flap events are calculated (seconds). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">flap_rate</span> - Number of stage change events needed within flap-duration. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">flap_timeout</span> - Flap guard disabling protection (min). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">flap_trig</span> - Flag is set if triggered on this port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">flapguard</span> - Enable / disable FlapGuard. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">flapguard_state</span> - Timestamp of last triggered event (or 0 if none). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">flow_control</span> - Configure flow control pause frames. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, tx, rx, both</span> </li>
        <li> <span class="li-head">fortilink_p2p</span> - FortiLink point-to-point. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">l2_learning</span> - Enable / disable dynamic MAC address learning. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">l2_sa_unknown</span> - Forward / drop unknown(SMAC) packets when dynamic MAC address learning is disabled. <span class="li-normal">type: str</span> <span class="li-normal">choices: forward, drop</span> </li>
        <li> <span class="li-head">link_status</span> - Physical link status. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">lldp_profile</span> - LLDP port TLV profile. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">lldp_status</span> - LLDP transmit and receive status. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, rx-only, tx-only, tx-rx</span> </li>
        <li> <span class="li-head">loopback</span> - Phy Port Loopback. <span class="li-normal">type: str</span> <span class="li-normal">choices: local, remote, disable</span> </li>
        <li> <span class="li-head">macsec_pae_mode</span> - Assign PAE mode to a MACSEC interface. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, supp, auth</span> </li>
        <li> <span class="li-head">macsec_profile</span> - macsec port profile. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">max_frame_size</span> - Maximum frame size. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">medium</span> - Configure port preference for shared ports. <span class="li-normal">type: str</span> <span class="li-normal">choices: fiber-preferred, copper-preferred, fiber-forced, copper-forced</span> </li>
        <li> <span class="li-head">name</span> - Port name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">owning_interface</span> - Trunk interface. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">pause_meter_rate</span> - Configure ingress metering rate. In kbits. 0 = disabled. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">pause_resume</span> - Resume threshold for resuming reception on pause metering of an ingress port. <span class="li-normal">type: str</span> <span class="li-normal">choices: 75%, 50%, 25%</span> </li>
        <li> <span class="li-head">poe_port_mode</span> - IEEE802.3AF/IEEE802.3AT <span class="li-normal">type: str</span> <span class="li-normal">choices: IEEE802_3AF, IEEE802_3AT</span> </li>
        <li> <span class="li-head">poe_port_priority</span> - Configure port priority <span class="li-normal">type: str</span> <span class="li-normal">choices: low-priority, high-priority, critical-priority</span> </li>
        <li> <span class="li-head">poe_status</span> - Enable/disable PSE. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">port_index</span> - Port index. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">priority_based_flow_control</span> - Enable / disable priority-based flow control. 802.3 flow control will be applied when disabled <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">qsfp_low_power_mode</span> - Enable/Disable QSFP low power mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: enabled, disabled</span> </li>
        <li> <span class="li-head">security_mode</span> - Security mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, macsec</span> </li>
        <li> <span class="li-head">speed</span> - Configure interface speed and duplex. <span class="li-normal">type: str</span> <span class="li-normal">choices: auto, 10half, 10full, 100half, 100full, 100FX-half, 100FX-full, 1000full, 2500auto, 5000auto, 10000full, 10000cr, 10000sr, 40000full, 40000sr4, 40000cr4, 100000full, 100000cr4, 100000sr4, auto-module, 1000full-fiber, 1000auto, 25000full, 25000cr, 25000sr, 50000full, 50000cr, 50000sr, 2500full, 40000auto</span> </li>
        <li> <span class="li-head">status</span> - Administrative status. <span class="li-normal">type: str</span> <span class="li-normal">choices: up, down</span> </li>
        <li> <span class="li-head">storm_control</span> - Storm control. <span class="li-normal">type: dict</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">broadcast</span> - Enable/disable broadcast storm control. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">burst_size_level</span> - Storm control burst size level 0-4. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">rate</span> - Storm control traffic rate. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">unknown_multicast</span> - Enable/disable unknown multicast storm control. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">unknown_unicast</span> - Enable/disable unknown unicast storm control. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">storm_control_mode</span> - Storm control mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: global, override, disabled</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Physical port specific configuration.
      fortinet.fortiswitch.fortiswitch_switch_physical_port:
          state: "present"
          switch_physical_port:
              cdp_status: "disable"
              description: "<your_own_value>"
              dmi_status: "enable"
              eee_tx_idle_time: "6"
              eee_tx_wake_time: "7"
              egress_drop_mode: "enabled"
              energy_efficient_ethernet: "enable"
              flap_duration: "10"
              flap_rate: "11"
              flap_timeout: "12"
              flap_trig: "13"
              flapguard: "enabled"
              flapguard_state: "<your_own_value>"
              flow_control: "disable"
              fortilink_p2p: "enable"
              l2_learning: "enabled"
              l2_sa_unknown: "forward"
              link_status: "<your_own_value>"
              lldp_profile: "<your_own_value> (source switch.lldp.profile.name)"
              lldp_status: "disable"
              loopback: "local"
              macsec_pae_mode: "none"
              macsec_profile: "<your_own_value> (source switch.macsec.profile.name)"
              max_frame_size: "26"
              medium: "fiber-preferred"
              name: "default_name_28"
              owning_interface: "<your_own_value>"
              pause_meter_rate: "30"
              pause_resume: "75%"
              poe_port_mode: "IEEE802_3AF"
              poe_port_priority: "low-priority"
              poe_status: "enable"
              port_index: "35"
              priority_based_flow_control: "disable"
              qsfp_low_power_mode: "enabled"
              security_mode: "none"
              speed: "auto"
              status: "up"
              storm_control:
                  broadcast: "enable"
                  burst_size_level: "43"
                  rate: "44"
                  unknown_multicast: "enable"
                  unknown_unicast: "enable"
              storm_control_mode: "global"


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
