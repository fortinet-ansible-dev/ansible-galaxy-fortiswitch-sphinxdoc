:source: fortiswitch_system_global.py

:orphan:

.. fortiswitch_system_global:

fortiswitch_system_global -- Configure global range attributes in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and global category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_global</td>
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
    <li> <span class="li-head">system_global</span> - Configure global range attributes. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">admin_concurrent</span> - Enable/disable concurrent login of adminstrative users. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">admin_https_pki_required</span> - Enable/disable HTTPS login page when PKI is enabled. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">admin_https_ssl_versions</span> - Allowed SSL/TLS versions for web administration. <span class="li-normal">type: str</span> <span class="li-normal">choices: tlsv1-0, tlsv1-1, tlsv1-2, tlsv1-3</span> </li>
        <li> <span class="li-head">admin_lockout_duration</span> - Lockout duration for FortiSwitch administration (1 - 2147483647 sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">admin_lockout_threshold</span> - Lockout threshold for FortiSwitch administration. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">admin_password_hash</span> - Admin password hash algorithm. (sha1, sha256, pbkdf2) <span class="li-normal">type: str</span> <span class="li-normal">choices: sha1, sha256, pbkdf2, pbkdf2-high</span> </li>
        <li> <span class="li-head">admin_port</span> - Administrative access HTTP port (1 - 65535). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">admin_restrict_local</span> - Enable/disable local admin authentication restriction when remote authenticator is up and running. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">admin_scp</span> - Enable/disable downloading of system configuraiton using SCP. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">admin_server_cert</span> - Administrative HTTPS server certificate. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">admin_sport</span> - Administrative access HTTPS port (1 - 65535). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">admin_ssh_grace_time</span> - Administrative access login grace time (10 - 3600 sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">admin_ssh_port</span> - Administrative access SSH port (1 - 65535). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">admin_ssh_v1</span> - Enable/disable SSH v1 compatibility. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">admin_telnet_port</span> - Administrative access TELNET port (1 - 65535). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">admintimeout</span> - Idle time-out for firewall administration. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">alert_interval</span> - Interval between each syslog entry when a sensor is out-of-range with respect to its threshold (in mins). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">alertd_relog</span> - Enable/disable re-logs when a sensor exceeds it"s threshold. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">allow_subnet_overlap</span> - Enable/disable subnet overlap. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">arp_inspection_monitor_timeout</span> - Timeout used when MAC-VLAN-IP learned from ARP traffic. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">arp_timeout</span> - ARP timeout value in seconds. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">asset_tag</span> - Asset tag. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auto_isl</span> - Enable/disable automatic inter-switch LAG. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">ca_certificate_802dot1x</span> - CA certificate for Port Security (802.1x). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">certificate_802dot1x</span> - Certificate for Port Security (802.1x). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">cfg_revert_timeout</span> - Time-out for reverting to the last saved configuration (10 - 2147483647). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">cfg_save</span> - Configure configuration saving mode (valid only for changes made in the CLI). <span class="li-normal">type: str</span> <span class="li-normal">choices: automatic, manual, revert</span> </li>
        <li> <span class="li-head">clt_cert_req</span> - Enable the requirement of client certificate for GUI login. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">csr_ca_attribute</span> - Enable/disable CA attribute in CSR. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">daily_restart</span> - Enable/disable FortiSwitch daily reboot. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">delaycli_timeout_cleanup</span> - Time-out for cleaning up the delay cli execution completion data (1-1440 minutes). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">detect_ip_conflict</span> - Enable/disable detection of IP address conflicts. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">dh_params</span> - Minimum size of Diffie-Hellman prime for HTTPS/SSH (bits). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcp_circuit_id</span> - List the parameters to be included to inform about client identification. <span class="li-normal">type: str</span> <span class="li-normal">choices: intfname, vlan, hostname, mode, description</span> </li>
        <li> <span class="li-head">dhcp_client_location</span> - List the parameters to be included to inform about client location. <span class="li-normal">type: str</span> <span class="li-normal">choices: intfname, vlan, hostname, mode, description</span> </li>
        <li> <span class="li-head">dhcp_option_format</span> - DHCP Option format string. <span class="li-normal">type: str</span> <span class="li-normal">choices: legacy, ascii</span> </li>
        <li> <span class="li-head">dhcp_remote_id</span> - List the parameters to be included in remote-id field. <span class="li-normal">type: str</span> <span class="li-normal">choices: mac, hostname, ip</span> </li>
        <li> <span class="li-head">dhcp_server_access_list</span> - Enable/Disable trusted DHCP Server list. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">dhcp_snoop_client_req</span> - Client DHCP packet broadcast mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: forward-untrusted, drop-untrusted</span> </li>
        <li> <span class="li-head">dhcps_db_exp</span> - Expiry time for dhcp-snoop server-db entry (300-259200 sec). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dhcps_db_per_port_learn_limit</span> - Per Interface dhcp-server entries learn limit . <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">dst</span> - Enable/disable daylight saving time. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">failtime</span> - Fail-time for PING server lost. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">fortilink_auto_discovery</span> - Enable/disable automatic discovery of FortiLink. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">hostname</span> - FortiSwitch hostname. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">image_rotation</span> - Enable/disable image upgrade partition rotation. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">interval</span> - Dead gateway detection interval. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ip_conflict_ignore_default</span> - Enable/disable IP conflict detection for default IP address. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">ipv6_accept_dad</span> - Whether to accept ipv6 DAD (Duplicate Address Detection). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">ipv6_all_forwarding</span> - Enable/disable ipv6 all forwarding. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">kernel_crashlog</span> - Enable/disable capture of kernel error messages to crash log. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">kernel_devicelog</span> - Enable/disable capture of kernel device messages to log. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">l3_host_expiry</span> - Enable/disable l3 host expiry. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">language</span> - GUI display language. <span class="li-normal">type: str</span> <span class="li-normal">choices: browser, english, simch, japanese, korean, spanish, trach, french, portuguese, german</span> </li>
        <li> <span class="li-head">ldapconntimeout</span> - LDAP connection time-out (0 - 2147483647 milliseconds). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">post_login_banner</span> - System post-login banner message. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">pre_login_banner</span> - System pre-login banner message. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">private_data_encryption</span> - Enable/disable private data encryption using an AES 128-bit key. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">radius_coa_port</span> - RADIUS CoA port number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">radius_port</span> - RADIUS server port number. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">remoteauthtimeout</span> - Remote authentication (RADIUS/LDAP) time-out (0 - 300). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">reset_button</span> - When disabled, reset is ignored while the OS is running. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">restart_time</span> - Daily restart time <hh:mm>. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">revision_backup_on_logout</span> - Enable/disable automatic revision backup upon logout. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">revision_backup_on_upgrade</span> - Enable/disable automatic revision backup upon upgrade of system image. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">strong_crypto</span> - Enable/disable strong cryptography for HTTPS/SSH access. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">switch_mgmt_mode</span> - Switch mode setting. <span class="li-normal">type: str</span> <span class="li-normal">choices: local, fortilink</span> </li>
        <li> <span class="li-head">tcp6_mss_min</span> - Minimum allowed TCP MSS value in bytes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">tcp_mss_min</span> - Minimum allowed TCP MSS value in bytes. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">tcp_options</span> - Enable/disable TCP options (timestamps, SACK, window scaling). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">tftp</span> - Enable/disable TFTP. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">timezone</span> - Time zone. <span class="li-normal">type: str</span> <span class="li-normal">choices: 01, 02, 03, 04, 05, 81, 06, 07, 08, 09, 10, 11, 12, 13, 74, 14, 77, 15, 87, 16, 17, 18, 19, 20, 75, 21, 22, 23, 24, 80, 79, 25, 26, 27, 28, 78, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 83, 84, 40, 85, 41, 42, 43, 39, 44, 46, 47, 51, 48, 45, 49, 50, 52, 53, 54, 55, 56, 57, 58, 59, 60, 62, 63, 61, 64, 65, 66, 67, 68, 69, 70, 71, 72, 00, 82, 73, 86, 76, 88, 89, 90, 91, 92</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Configure global range attributes.
      fortinet.fortiswitch.fortiswitch_system_global:
          system_global:
              802.1x_ca_certificate: "<your_own_value>"
              802.1x_certificate: "<your_own_value>"
              admin_concurrent: "enable"
              admin_https_pki_required: "enable"
              admin_https_ssl_versions: "tlsv1-0"
              admin_lockout_duration: "1073741823"
              admin_lockout_threshold: "9"
              admin_password_hash: "sha1"
              admin_port: "32767"
              admin_restrict_local: "enable"
              admin_scp: "enable"
              admin_server_cert: "<your_own_value>"
              admin_sport: "32767"
              admin_ssh_grace_time: "1800"
              admin_ssh_port: "32767"
              admin_ssh_v1: "enable"
              admin_telnet_port: "32767"
              admintimeout: "20"
              alert_interval: "21"
              alertd_relog: "enable"
              allow_subnet_overlap: "enable"
              arp_inspection_monitor_timeout: "5040"
              arp_timeout: "25"
              asset_tag: "<your_own_value>"
              auto_isl: "enable"
              cfg_revert_timeout: "1073741823"
              cfg_save: "automatic"
              clt_cert_req: "enable"
              csr_ca_attribute: "enable"
              daily_restart: "enable"
              delaycli_timeout_cleanup: "33"
              detect_ip_conflict: "enable"
              dh_params: "35"
              dhcp_circuit_id: "intfname"
              dhcp_client_location: "intfname"
              dhcp_option_format: "legacy"
              dhcp_remote_id: "mac"
              dhcp_server_access_list: "enable"
              dhcp_snoop_client_req: "forward-untrusted"
              dhcps_db_exp: "129600"
              dhcps_db_per_port_learn_limit: "512"
              dst: "enable"
              failtime: "45"
              fortilink_auto_discovery: "enable"
              hostname: "myhostname"
              image_rotation: "disable"
              interval: "49"
              ip_conflict_ignore_default: "enable"
              ipv6_accept_dad: "1"
              ipv6_all_forwarding: "enable"
              kernel_crashlog: "enable"
              kernel_devicelog: "enable"
              l3_host_expiry: "enable"
              language: "browser"
              ldapconntimeout: "1073741823"
              post_login_banner: "<your_own_value>"
              pre_login_banner: "<your_own_value>"
              private_data_encryption: "disable"
              radius_coa_port: "61"
              radius_port: "62"
              remoteauthtimeout: "150"
              reset_button: "enable"
              restart_time: "<your_own_value>"
              revision_backup_on_logout: "enable"
              revision_backup_on_upgrade: "enable"
              strong_crypto: "enable"
              switch_mgmt_mode: "local"
              tcp6_mss_min: "70"
              tcp_mss_min: "71"
              tcp_options: "enable"
              tftp: "enable"
              timezone: "01"


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
