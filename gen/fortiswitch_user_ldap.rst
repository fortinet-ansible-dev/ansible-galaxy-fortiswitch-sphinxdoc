:source: fortiswitch_user_ldap.py

:orphan:

.. fortiswitch_user_ldap:

fortiswitch_user_ldap -- LDAP server entry configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify user feature and ldap category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_user_ldap</td>
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
    <li> <span class="li-head">user_ldap</span> - LDAP server entry configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">ca_cert</span> - CA certificate name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">cnid</span> - Common Name identifier . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">dn</span> - Distinguished name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">group_member_check</span> - Group member checking options. <span class="li-normal">type: str</span> <span class="li-normal">choices: user-attr, group-object</span> </li>
        <li> <span class="li-head">group_object_filter</span> - Group searching filter. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">member_attr</span> - Name of attribute from which to get group membership. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">name</span> - LDAP server entry name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">password</span> - Password for initial binding. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">password_expiry_warning</span> - Enable/disable password expiry warnings. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">password_renewal</span> - Enable/disable online password renewal. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">port</span> - LDAP server port number (1 - 65535). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">secure</span> - SSL connection. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, starttls, ldaps</span> </li>
        <li> <span class="li-head">server</span> - LDAP server domain name or IP address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">server_identity_check</span> - Enable/disable LDAP server identity check (verify server domain name/IP address against the server certificate). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">type</span> - LDAP binding type. <span class="li-normal">type: str</span> <span class="li-normal">choices: simple, anonymous, regular</span> </li>
        <li> <span class="li-head">username</span> - Username (full DN) for initial binding. <span class="li-normal">type: str</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: LDAP server entry configuration.
      fortinet.fortiswitch.fortiswitch_user_ldap:
          state: "present"
          user_ldap:
              ca_cert: "<your_own_value> (source system.certificate.ca.name)"
              cnid: "<your_own_value>"
              dn: "<your_own_value>"
              group_member_check: "user-attr"
              group_object_filter: "<your_own_value>"
              member_attr: "<your_own_value>"
              name: "default_name_9"
              password: "<your_own_value>"
              password_expiry_warning: "enable"
              password_renewal: "enable"
              port: "32767"
              secure: "disable"
              server: "192.168.100.40"
              server_identity_check: "enable"
              type: "simple"
              username: "<your_own_value>"


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
