:source: fortiswitch_alertemail_setting.py

:orphan:

.. fortiswitch_alertemail_setting:

fortiswitch_alertemail_setting -- Alertemail setting configuration in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify alertemail feature and setting category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_alertemail_setting</td>
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
    <li> <span class="li-head">alertemail_setting</span> - Alertemail setting configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">admin_login_logs</span> - Admin-login-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">alert_interval</span> - Set Alert alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">amc_interface_bypass_mode</span> - Amc-interface-bypass-mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">antivirus_logs</span> - Antivirus-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">configuration_changes_logs</span> - Configuration-changes-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">critical_interval</span> - Set Critical alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">debug_interval</span> - Set Debug alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">email_interval</span> - Interval between each email. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">emergency_interval</span> - Set Emergency alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">error_interval</span> - Set Error alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">FDS_license_expiring_days</span> - Send alertemail before these days FortiGuard license expire (1-100). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">FDS_license_expiring_warning</span> - FDS-license-expiring-warning. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">FDS_update_logs</span> - FDS-update-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">filter_mode</span> - Filter mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: category, threshold</span> </li>
        <li> <span class="li-head">firewall_authentication_failure_logs</span> - Firewall-authentication-failure-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">fortiguard_log_quota_warning</span> - Fortiguard-log-quota-warning. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">HA_logs</span> - HA-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">information_interval</span> - Set Information alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">IPS_logs</span> - IPS-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">IPsec_errors_logs</span> - IPsec-errors-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">local_disk_usage</span> - Send alertemail when disk usage exceeds this threshold (1-99). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">log_disk_usage_warning</span> - Log-disk-usage-warning. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">mailto1</span> - Set destination email address 1. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">mailto2</span> - Set destination email address 2. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">mailto3</span> - Set destination email address 3. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">notification_interval</span> - Set Notification alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">PPP_errors_logs</span> - PPP-errors-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">severity</span> - The least severity level to log. <span class="li-normal">type: str</span> <span class="li-normal">choices: emergency, alert, critical, error, warning, notification, information, debug</span> </li>
        <li> <span class="li-head">sslvpn_authentication_errors_logs</span> - Sslvpn-authentication-errors-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">username</span> - Set email from address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">violation_traffic_logs</span> - Violation-traffic-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">warning_interval</span> - Set Warning alert interval in minutes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">webfilter_logs</span> - Webfilter-logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Alertemail setting configuration.
      fortinet.fortiswitch.fortiswitch_alertemail_setting:
          alertemail_setting:
              admin_login_logs: "enable"
              alert_interval: "4"
              amc_interface_bypass_mode: "enable"
              antivirus_logs: "enable"
              configuration_changes_logs: "enable"
              critical_interval: "8"
              debug_interval: "9"
              email_interval: "10"
              emergency_interval: "11"
              error_interval: "12"
              FDS_license_expiring_days: "13"
              FDS_license_expiring_warning: "enable"
              FDS_update_logs: "enable"
              filter_mode: "category"
              firewall_authentication_failure_logs: "enable"
              fortiguard_log_quota_warning: "enable"
              HA_logs: "enable"
              information_interval: "20"
              IPS_logs: "enable"
              IPsec_errors_logs: "enable"
              local_disk_usage: "23"
              log_disk_usage_warning: "enable"
              mailto1: "<your_own_value>"
              mailto2: "<your_own_value>"
              mailto3: "<your_own_value>"
              notification_interval: "28"
              PPP_errors_logs: "enable"
              severity: "emergency"
              sslvpn_authentication_errors_logs: "enable"
              username: "<your_own_value>"
              violation_traffic_logs: "enable"
              warning_interval: "34"
              webfilter_logs: "enable"


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
