:source: fortiswitch_system_admin.py

:orphan:

.. fortiswitch_system_admin:

fortiswitch_system_admin -- Administrative user configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and admin category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_admin</td>
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
    <li> <span class="li-head">system_admin</span> - Administrative user configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">accprofile</span> - Administrative user access profile. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">accprofile_override</span> - Enable/disable remote authentication server to override access profile. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">allow_remove_admin_session</span> - Enable/disable privileged administrative users to remove administrative sessions. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">comments</span> - Comment. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">email_address</span> - Email address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">first_name</span> - First name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">force_password_change</span> - Enable/disable forcing of password change on next login. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">hidden</span> - Administrative user hidden attribute. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ip6_trusthost1</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost10</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost2</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost3</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost4</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost5</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost6</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost7</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost8</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ip6_trusthost9</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">is_admin</span> - User has administrative privileges. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">last_name</span> - Last name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">mobile_number</span> - Mobile number. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">name</span> - Adminstrative user name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">pager_number</span> - Pager number. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">password</span> - Remote authentication password. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">password_expire</span> - Password expire time. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">peer_auth</span> - Enable/disable peer authentication. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">peer_group</span> - Peer group name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">phone_number</span> - Phone number. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">remote_auth</span> - Enable/disable remote authentication. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">remote_group</span> - Remote authentication group name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">schedule</span> - Schedule name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ssh_public_key1</span> - SSH public key1. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ssh_public_key2</span> - SSH public key2. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ssh_public_key3</span> - SSH public key3. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost1</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost10</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost2</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost3</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost4</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost5</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost6</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost7</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost8</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">trusthost9</span> - Trusted host one IP address . <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">vdom</span> - Virtual domain name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">wildcard</span> - Enable/disable wildcard RADIUS authentication. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">wildcard_fallback</span> - Enable/disable attempting authentication against wildcard accounts if authenticating this account fails. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Administrative user configuration.
      fortinet.fortiswitch.fortiswitch_system_admin:
          state: "present"
          system_admin:
              accprofile: "<your_own_value> (source system.accprofile.name)"
              accprofile_override: "enable"
              allow_remove_admin_session: "enable"
              comments: "<your_own_value>"
              Email address.: "<your_own_value>"
              First name.: "<your_own_value>"
              force_password_change: "enable"
              hidden: "10"
              ip6_trusthost1: "<your_own_value>"
              ip6_trusthost10: "<your_own_value>"
              ip6_trusthost2: "<your_own_value>"
              ip6_trusthost3: "<your_own_value>"
              ip6_trusthost4: "<your_own_value>"
              ip6_trusthost5: "<your_own_value>"
              ip6_trusthost6: "<your_own_value>"
              ip6_trusthost7: "<your_own_value>"
              ip6_trusthost8: "<your_own_value>"
              ip6_trusthost9: "<your_own_value>"
              is_admin: "21"
              Last name.: "<your_own_value>"
              Mobile number.: "<your_own_value>"
              name: "default_name_24"
              Pager number.: "<your_own_value>"
              password: "<your_own_value>"
              password_expire: "<your_own_value>"
              peer_auth: "enable"
              peer_group: "<your_own_value>"
              Phone number.: "<your_own_value>"
              remote_auth: "enable"
              remote_group: "<your_own_value>"
              schedule: "<your_own_value>"
              ssh_public_key1: "<your_own_value>"
              ssh_public_key2: "<your_own_value>"
              ssh_public_key3: "<your_own_value>"
              trusthost1: "<your_own_value>"
              trusthost10: "<your_own_value>"
              trusthost2: "<your_own_value>"
              trusthost3: "<your_own_value>"
              trusthost4: "<your_own_value>"
              trusthost5: "<your_own_value>"
              trusthost6: "<your_own_value>"
              trusthost7: "<your_own_value>"
              trusthost8: "<your_own_value>"
              trusthost9: "<your_own_value>"
              vdom: "<your_own_value> (source system.vdom.name)"
              wildcard: "enable"
              wildcard_fallback: "enable"


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
