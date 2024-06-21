:source: fortiswitch_system_certificate_crl.py

:orphan:

.. fortiswitch_system_certificate_crl:

fortiswitch_system_certificate_crl -- Certificate Revokation List in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system_certificate feature and crl category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_certificate_crl</td>
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
    <li> <span class="li-head">system_certificate_crl</span> - Certificate Revokation List. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">crl</span> - Certificate Revocation List. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">http_url</span> - URL of HTTP server for CRL update. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ldap_password</span> - Login password for LDAP server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ldap_server</span> - LDAP server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ldap_username</span> - Login name for LDAP server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">scep_cert</span> - Local certificate used for CRL update via SCEP. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">scep_url</span> - URL of CA server for CRL update via SCEP. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">update_interval</span> - Second between updates, 0=disabled. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">update_vdom</span> - Virtual domain for CRL update. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Certificate Revokation List.
      fortinet.fortiswitch.fortiswitch_system_certificate_crl:
          state: "present"
          system_certificate_crl:
              crl: "<your_own_value>"
              http_url: "<your_own_value>"
              ldap_password: "<your_own_value>"
              ldap_server: "<your_own_value>"
              ldap_username: "<your_own_value>"
              name: "default_name_8"
              scep_cert: "<your_own_value>"
              scep_url: "<your_own_value>"
              update_interval: "11"
              update_vdom: "<your_own_value> (source system.vdom.name)"


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
