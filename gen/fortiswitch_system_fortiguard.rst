:source: fortiswitch_system_fortiguard.py

:orphan:

.. fortiswitch_system_fortiguard:

fortiswitch_system_fortiguard -- Configure FortiGuard services in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and fortiguard category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_fortiguard</td>
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
    <li> <span class="li-head">system_fortiguard</span> - Configure FortiGuard services. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">analysis_service</span> - Enable or disable the analysis service. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">antispam_cache</span> - Enable/disable the cache. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">antispam_cache_mpercent</span> - The maximum percent of memory the cache is allowed to use (1-15%). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">antispam_cache_ttl</span> - The time-to-live for cache entries in seconds (300-86400). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">antispam_expiration</span> - When license will expire. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">antispam_force_off</span> - Forcibly disable the service. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">antispam_license</span> - License type. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">antispam_score_threshold</span> - Antispam score threshold [50,100]. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">antispam_timeout</span> - Query time out (1-30 seconds). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">avquery_cache</span> - Enable/disable the cache. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">avquery_cache_mpercent</span> - The maximum percent of memory the cache is allowed to use (1-15%). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">avquery_cache_ttl</span> - The time-to-live for cache entries in seconds (300-86400). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">avquery_expiration</span> - When license will expire. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">avquery_force_off</span> - Forcibly disable the service. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">avquery_license</span> - License type. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">avquery_timeout</span> - Query time out (1-30 seconds). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">client_override_ip</span> - Client override IP address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">client_override_status</span> - Enable or disable the client override IP. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">hostname</span> - Hostname or IP of the FortiGuard server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">load_balance_servers</span> - Number of servers to alternate between as first Fortiguard option. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">port</span> - Port used to communicate with the FortiGuard servers. <span class="li-normal">type: str</span> <span class="li-normal">choices: 53, 8888</span> </li>
        <li> <span class="li-head">service_account_id</span> - Service account id. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">srv_ovrd</span> - Enable or disable the server override list. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">srv_ovrd_list</span> - Configure the server override list. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">addr_type</span> - Type of address. <span class="li-normal">type: str</span> <span class="li-normal">choices: ipv4, ipv6</span> </li>
            <li> <span class="li-head">ip</span> - Override server IP address. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">ip6</span> - Override server IP6 address. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">webfilter_cache</span> - Enable/disable the cache. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">webfilter_cache_ttl</span> - The time-to-live for cache entries in seconds (300-86400). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">webfilter_expiration</span> - When license will expire. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">webfilter_force_off</span> - Forcibly disable the service. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">webfilter_license</span> - License type. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">webfilter_timeout</span> - Query time out (1-30 seconds). <span class="li-normal">type: int</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Configure FortiGuard services.
      fortinet.fortiswitch.fortiswitch_system_fortiguard:
          system_fortiguard:
              analysis_service: "enable"
              antispam_cache: "enable"
              antispam_cache_mpercent: "7"
              antispam_cache_ttl: "6"
              antispam_expiration: "7"
              antispam_force_off: "enable"
              antispam_license: "9"
              antispam_score_threshold: "10"
              antispam_timeout: "15"
              avquery_cache: "enable"
              avquery_cache_mpercent: "7"
              avquery_cache_ttl: "14"
              avquery_expiration: "15"
              avquery_force_off: "enable"
              avquery_license: "17"
              avquery_timeout: "15"
              client_override_ip: "<your_own_value>"
              client_override_status: "enable"
              hostname: "myhostname"
              load_balance_servers: "25"
              port: "53"
              service_account_id: "<your_own_value>"
              srv_ovrd: "enable"
              srv_ovrd_list:
                  -
                      addr_type: "ipv4"
                      ip: "<your_own_value>"
                      ip6: "<your_own_value>"
              webfilter_cache: "enable"
              webfilter_cache_ttl: "31"
              webfilter_expiration: "32"
              webfilter_force_off: "enable"
              webfilter_license: "34"
              webfilter_timeout: "15"


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
