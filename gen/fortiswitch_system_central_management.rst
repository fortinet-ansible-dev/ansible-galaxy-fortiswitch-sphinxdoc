:source: fortiswitch_system_central_management.py

:orphan:

.. fortiswitch_system_central_management:

fortiswitch_system_central_management -- Central management configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and central_management category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td><code class="docutils literal notranslate">v7.0.4 </code></td>
 <td><code class="docutils literal notranslate">v7.0.5 </code></td>
 <td><code class="docutils literal notranslate">v7.0.6 </code></td>
 </tr>
 <tr>
 <td>fortiswitch_system_central_management</td>
 <td>yes</td>
 <td>yes</td>
 <td>yes</td>
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
    <li> <span class="li-head">system_central_management</span> - Central management configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">allow_monitor</span> - Enable/disable remote monitor of device. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">allow_push_configuration</span> - Enable/disable push configuration. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">allow_pushd_firmware</span> - Enable/disable push firmware. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">allow_remote_firmware_upgrade</span> - Enable/disable push firmware. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">enc_algorithm</span> - Whether to use SSL encryption. <span class="li-normal">type: str</span> <span class="li-normal">choices: default, high, low</span> </li>
        <li> <span class="li-head">fmg</span> - Address of fortimanager(ip or fqdn name). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">fmg_source_ip</span> - Source address to use when connecting fortimanager. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">mode</span> - Normal/backup management mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: normal, backup</span> </li>
        <li> <span class="li-head">schedule_config_restore</span> - Enable/disable schedule config restore. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">schedule_script_restore</span> - Enable/disable schedule config restore. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">serial_number</span> - Serial number. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable management. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">type</span> - Type of management server. <span class="li-normal">type: str</span> <span class="li-normal">choices: fortimanager, fortiguard</span> </li>
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
      - name: Central management configuration.
        fortiswitch_system_central_management:
          system_central_management:
            allow_monitor: "enable"
            allow_push_configuration: "enable"
            allow_pushd_firmware: "enable"
            allow_remote_firmware_upgrade: "enable"
            enc_algorithm: "default"
            fmg: "<your_own_value>"
            fmg_source_ip: "<your_own_value>"
            mode: "normal"
            schedule_config_restore: "enable"
            schedule_script_restore: "enable"
            serial_number: "<your_own_value>"
            status: "enable"
            type: "fortimanager"
    


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
