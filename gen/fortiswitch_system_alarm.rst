:source: fortiswitch_system_alarm.py

:orphan:

.. fortiswitch_system_alarm:

fortiswitch_system_alarm -- Alarm configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and alarm category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_alarm</td>
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
    <li> <span class="li-head">system_alarm</span> - Alarm configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">audible</span> - Enable/disable audible alarm. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">groups</span> - Alarm groups. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">admin_auth_failure_threshold</span> - Admin authentication failure threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">admin_auth_lockout_threshold</span> - Admin authentication lockout threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">decryption_failure_threshold</span> - Decryption failure threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">encryption_failure_threshold</span> - Encryption failure threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">fw_policy_id</span> - Firewall policy id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">fw_policy_id_threshold</span> - Firewall policy id threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">fw_policy_violations</span> - Firewall policy violations. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">dst_ip</span> - Destination ip (0=all). <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">dst_port</span> - Destination port (0=all). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">src_ip</span> - Source ip (0=all). <span class="li-normal">type: str</span> </li>
                <li> <span class="li-head">src_port</span> - Source port (0=all). <span class="li-normal">type: int</span> </li>
                <li> <span class="li-head">threshold</span> - Firewall policy violation threshold. <span class="li-normal">type: int</span> </li>
                </ul>
            <li> <span class="li-head">id</span> - Group id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">log_full_warning_threshold</span> - Log full warning threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">period</span> - Time period in seconds (0=from start up). <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">replay_attempt_threshold</span> - Replay attempt threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">self_test_failure_threshold</span> - Self-test failure threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">user_auth_failure_threshold</span> - User authentication failure threshold. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">user_auth_lockout_threshold</span> - User authentication lockout threshold. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">sequence</span> - Sequence id of alarms. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable alarm. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Alarm configuration.
      fortinet.fortiswitch.fortiswitch_system_alarm:
          system_alarm:
              audible: "enable"
              groups:
                  -
                      admin_auth_failure_threshold: "5"
                      admin_auth_lockout_threshold: "6"
                      decryption_failure_threshold: "7"
                      encryption_failure_threshold: "8"
                      fw_policy_id: "2147483647"
                      fw_policy_id_threshold: "10"
                      fw_policy_violations:
                          -
                              dst_ip: "<your_own_value>"
                              dst_port: "32767"
                              src_ip: "<your_own_value>"
                              src_port: "32767"
                              threshold: "16"
                      id: "17"
                      log_full_warning_threshold: "18"
                      period: "2147483647"
                      replay_attempt_threshold: "20"
                      self_test_failure_threshold: "21"
                      user_auth_failure_threshold: "22"
                      user_auth_lockout_threshold: "23"
              sequence: "24"
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
    If you notice any issues in this documentation, feel free to create a pull request to improve it.
