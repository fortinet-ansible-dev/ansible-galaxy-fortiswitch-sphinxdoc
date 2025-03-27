:source: fortiswitch_switch_lldp_profile.py

:orphan:

.. fortiswitch_switch_lldp_profile:

fortiswitch_switch_lldp_profile -- LLDP configuration profiles in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_lldp feature and profile category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_lldp_profile</td>
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
    <li> <span class="li-head">switch_lldp_profile</span> - LLDP configuration profiles. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">auto_isl</span> - Enable/disable automatic inter-switch LAG. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">auto_isl_auth</span> - Automatic inter-switch LAG authentication. <span class="li-normal">type: str</span> <span class="li-normal">choices: legacy, strict, relax</span> </li>
        <li> <span class="li-head">auto_isl_auth_encrypt</span> - Automatic inter-switch LAG authentication encryption. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, must, mixed</span> </li>
        <li> <span class="li-head">auto_isl_auth_identity</span> - Automatic authentication identity. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auto_isl_auth_macsec_profile</span> - Fortilink LLDP macsec port profile. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auto_isl_auth_reauth</span> - Automatic authentication reauth period (10 - 3600 mins). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">auto_isl_auth_user</span> - Automatic authentication User certificate. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auto_isl_hello_timer</span> - Automatic ISL hello timer (1 - 30 sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">auto_isl_port_group</span> - Automatic inter-switch LAG port group. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">auto_isl_receive_timeout</span> - Automatic ISL timeout (0 - 300 sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">auto_mclag_icl</span> - Enable/disable MCLAG inter chassis link. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">custom_tlvs</span> - Organizationally Specific TLV configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">information_string</span> - Organizationally defined information string. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">name</span> - TLV name (not sent). <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">oui</span> - Organizationally unique identifier. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">subtype</span> - Organizationally defined subtype. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">med_location_service</span> - LLDP MED location service configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Policy type name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - Enable/disable Location Service TLV. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">sys_location_id</span> - LLDP System Location Id. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">med_network_policy</span> - LLDP MED network policy configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">assign_vlan</span> - Enable/disable automatically adding this VLAN to ports with this profile (does not affect trunks). <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">dscp</span> - Advertised DSCP value. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - Policy type name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">priority</span> - Advertised L2 priority. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">status</span> - Enable/disable this TLV. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">vlan</span> - VLAN to advertise (if configured on port). <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">med_tlvs</span> - Transmitted LLDP-MED TLVs. <span class="li-normal">type: str</span> <span class="li-normal">choices: inventory-management, network-policy, location-identification, power-management</span> </li>
        <li> <span class="li-head">name</span> - Profile name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">tlvs_802dot1</span> - Transmitted IEEE 802.1 TLVs. <span class="li-normal">type: str</span> <span class="li-normal">choices: port-vlan-id, vlan-name</span> </li>
        <li> <span class="li-head">tlvs_802dot3</span> - Transmitted IEEE 802.3 TLVs. <span class="li-normal">type: str</span> <span class="li-normal">choices: max-frame-size, power-negotiation, eee-config</span> </li>
        <li> <span class="li-head">vlan_name_map</span> - VLANs that advertise Vlan Names <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: LLDP configuration profiles.
      fortinet.fortiswitch.fortiswitch_switch_lldp_profile:
          state: "present"
          switch_lldp_profile:
              802.1_tlvs: "port-vlan-id"
              802.3_tlvs: "max-frame-size"
              auto_isl: "enable"
              auto_isl_auth: "legacy"
              auto_isl_auth_encrypt: "none"
              auto_isl_auth_identity: "<your_own_value>"
              auto_isl_auth_macsec_profile: "<your_own_value> (source switch.macsec.profile.name)"
              auto_isl_auth_reauth: "1800"
              auto_isl_auth_user: "<your_own_value> (source system.certificate.local.name)"
              auto_isl_hello_timer: "15"
              auto_isl_port_group: "4"
              auto_isl_receive_timeout: "150"
              auto_mclag_icl: "enable"
              custom_tlvs:
                  -
                      information_string: "<your_own_value>"
                      name: "default_name_18"
                      oui: "<your_own_value>"
                      subtype: "127"
              med_location_service:
                  -
                      name: "default_name_22"
                      status: "disable"
                      sys_location_id: "<your_own_value> (source system.location.name)"
              med_network_policy:
                  -
                      assign_vlan: "disable"
                      dscp: "31"
                      name: "default_name_28"
                      priority: "3"
                      status: "disable"
                      vlan: "2047"
              med_tlvs: "inventory-management"
              name: "default_name_33"
              vlan_name_map: "<your_own_value>"


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
