:source: fortiswitch_switch_macsec_profile.py

:orphan:

.. fortiswitch_switch_macsec_profile:

fortiswitch_switch_macsec_profile -- MACsec configuration profiles in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_macsec feature and profile category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



Requirements
------------
The below requirements are needed on the host that executes this module.

- ansible>=2.11


FortiSW Version Compatibility
-----------------------------


.. raw:: html

 <br>
 <table>
 <tr>
 <td></td>
 <td><code class="docutils literal notranslate">v7.0.0 </code></td>
 <td><code class="docutils literal notranslate">v7.0.1 </code></td>
 <td><code class="docutils literal notranslate">v7.0.2 </code></td>
 <td><code class="docutils literal notranslate">v7.0.3 </code></td>
 </tr>
 <tr>
 <td>fortiswitch_switch_macsec_profile</td>
 <td>yes</td>
 <td>yes</td>
 <td>yes</td>
 <td>yes</td>
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
    <li> <span class="li-head">switch_macsec_profile</span> - MACsec configuration profiles. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">cipher_suite</span> - MACsec cipher suite. <span class="li-normal">type: str</span> <span class="li-normal">choices: GCM_AES_128</span> </li>
        <li> <span class="li-head">confident_offset</span> - Choose different confident offset bytes. <span class="li-normal">type: str</span> <span class="li-normal">choices: 0, 30, 50</span> </li>
        <li> <span class="li-head">encrypt_traffic</span> - Enable/disable Encryption of MACsec traffic. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">include_macsec_sci</span> - Include MACsec TX SCI. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">include_mka_icv_ind</span> - Include MKA ICV indicator. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable</span> </li>
        <li> <span class="li-head">macsec_mode</span> - Set mode of the MACsec Profile. <span class="li-normal">type: str</span> <span class="li-normal">choices: static-cak</span> </li>
        <li> <span class="li-head">macsec_validate</span> - Choose different MACsec validate mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: strict</span> </li>
        <li> <span class="li-head">mka_priority</span> - MACsec MKA priority. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mka_psk</span> - MACsec MKA pre-shared key configuration. <span class="li-normal">type: list</span> <span style="font-family:'Courier New'" class="li-required">member_path: mka_psk:name</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">crypto_alg</span> - PSK crypto algorithm. <span class="li-normal">type: str</span> <span class="li-normal">choices: AES_128_CMAC</span> </li>
            <li> <span class="li-head">mka_cak</span> - MKA CAK pre-shared key hex string. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">mka_ckn</span> - MKA CKN pre-shared key hex string. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">name</span> - pre-shared-key name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
            <li> <span class="li-head">status</span> - Status of this PSK. <span class="li-normal">type: str</span> <span class="li-normal">choices: active</span> </li>
            </ul>
        <li> <span class="li-head">name</span> - Profile name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">replay_protect</span> - Enable/disable MACsec replay protection. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">replay_window</span> - MACsec replay window size. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable this Profile. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">traffic_policy</span> - MACsec traffic policy configuration. <span class="li-normal">type: list</span> <span style="font-family:'Courier New'" class="li-required">member_path: traffic_policy:name</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">name</span> - Traffic policy type name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
            <li> <span class="li-head">security_policy</span> - Must/Should secure the traffic. <span class="li-normal">type: str</span> <span class="li-normal">choices: must-secure</span> </li>
            <li> <span class="li-head">status</span> - Enable/disable this Traffic policy. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable</span> </li>
            </ul>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - hosts: fortiswitch01
      collections:
        - fortinet.fortiswitch
      connection: httpapi
      vars:
       ansible_httpapi_use_ssl: yes
       ansible_httpapi_validate_certs: no
       ansible_httpapi_port: 443
      tasks:
      - name: MACsec configuration profiles.
        fortiswitch_switch_macsec_profile:
          state: "present"
          switch_macsec_profile:
            cipher_suite: "GCM_AES_128"
            confident_offset: "0"
            encrypt_traffic: "enable"
            include_macsec_sci: "enable"
            include_mka_icv_ind: "enable"
            macsec_mode: "static-cak"
            macsec_validate: "strict"
            mka_priority: "10"
            mka_psk:
             -
                crypto_alg: "AES_128_CMAC"
                mka_cak: "<your_own_value>"
                mka_ckn: "<your_own_value>"
                name: "default_name_15"
                status: "active"
            name: "default_name_17"
            replay_protect: "enable"
            replay_window: "19"
            status: "enable"
            traffic_policy:
             -
                name: "default_name_22"
                security_policy: "must-secure"
                status: "enable"
    


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
    If you notice any issues in this documentation, you can create a pull request to improve it.
