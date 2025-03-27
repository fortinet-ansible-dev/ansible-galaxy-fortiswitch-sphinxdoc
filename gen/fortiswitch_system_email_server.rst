:source: fortiswitch_system_email_server.py

:orphan:

.. fortiswitch_system_email_server:

fortiswitch_system_email_server -- Email server configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and email_server category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_email_server</td>
 <td><code class="docutils literal notranslate">v7.2.1 -> 7.4.3 </code></td>
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
    <li> <span class="li-head">system_email_server</span> - Email server configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">authenticate</span> - Enable/disable authentication. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">password</span> - Set SMTP server user password for authentication. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">port</span> - Set SMTP server port. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">reply_to</span> - Set Reply-To email address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">security</span> - Set connection security used by the email server. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, starttls, smtps</span> </li>
        <li> <span class="li-head">server</span> - Set SMTP server IP address or hostname. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">source_ip</span> - Set SMTP server IPv4 source IP. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">source_ip6</span> - Set SMTP server IPv6 source IP. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">ssl_min_proto_version</span> - Set minimum supported protocol version for SSL/TLS connections . <span class="li-normal">type: str</span> <span class="li-normal">choices: SSLv3, TLSv1, TLSv1-1, TLSv1-2, TLSv1-3</span> </li>
        <li> <span class="li-head">username</span> - Set SMTP server user name for authentication. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">validate_server</span> - Enable/disable validation of server certificate. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Email server configuration.
      fortinet.fortiswitch.fortiswitch_system_email_server:
          system_email_server:
              authenticate: "enable"
              password: "<your_own_value>"
              port: "32767"
              reply_to: "<your_own_value>"
              security: "none"
              server: "192.168.100.40"
              source_ip: "<your_own_value>"
              source_ip6: "<your_own_value>"
              ssl_min_proto_version: "SSLv3"
              username: "<your_own_value>"
              validate_server: "enable"


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
