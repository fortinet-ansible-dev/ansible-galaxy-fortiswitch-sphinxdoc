:source: fortiswitch_router_isis.py

:orphan:

.. fortiswitch_router_isis:

fortiswitch_router_isis -- ISIS configuration in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify router feature and isis category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_router_isis</td>
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
    <li> <span class="li-head">router_isis</span> - ISIS configuration. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">auth_keychain_area</span> - IS-IS area authentication key-chain. Applicable when area"s auth mode is md5. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auth_keychain_domain</span> - IS-IS domain authentication key-chain. Applicable when domain"s auth mode is md5. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auth_mode_area</span> - IS-IS area(level-1) authentication mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: password, md5</span> </li>
        <li> <span class="li-head">auth_mode_domain</span> - ISIS domain(level-2) authentication mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: password, md5</span> </li>
        <li> <span class="li-head">auth_password_area</span> - IS-IS area(level-1) authentication password. Applicable when area"s auth mode is password. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auth_password_domain</span> - IS-IS domain(level-2) authentication password. Applicable when domain"s auth mode is password. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">auth_sendonly_area</span> - Enable authentication send-only for level 1 SNP PDUs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">auth_sendonly_domain</span> - Enable authentication send-only for level 2 SNP PDUs. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">default_information_level</span> - Distribute default route into level"s LSP. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2</span> </li>
        <li> <span class="li-head">default_information_level6</span> - Distribute ipv6 default route into level"s LSP. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2</span> </li>
        <li> <span class="li-head">default_information_metric</span> - Default information metric. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">default_information_metric6</span> - Default ipv6 route metric. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">default_information_originate</span> - Enable/disable generation of default route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, always, disable</span> </li>
        <li> <span class="li-head">default_information_originate6</span> - Enable/disable generation of default ipv6 route. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, always, disable</span> </li>
        <li> <span class="li-head">ignore_attached_bit</span> - Ignore Attached bit on incoming L1 LSP. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">interface</span> - IS-IS interface configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">auth_keychain_hello</span> - Hello PDU authentication key-chain. Applicable when hello"s auth mode is md5. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">auth_mode_hello</span> - Hello PDU authentication mode. <span class="li-normal">type: str</span> <span class="li-normal">choices: md5, password</span> </li>
            <li> <span class="li-head">auth_password_hello</span> - Hello PDU authentication password. Applicable when hello"s auth mode is password. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">bfd</span> - Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">bfd6</span> - Ipv6 Bidirectional Forwarding Detection (BFD). <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">circuit_type</span> - IS-IS interface"s circuit type. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2</span> </li>
            <li> <span class="li-head">csnp_interval_l1</span> - Level 1 CSNP interval. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">csnp_interval_l2</span> - Level 2 CSNP interval. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_interval_l1</span> - Level 1 hello interval. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_interval_l2</span> - Level 2 hello interval. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_multiplier_l1</span> - Level 1 multiplier for Hello holding time. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_multiplier_l2</span> - Level 2 multiplier for Hello holding time. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">hello_padding</span> - Enable padding to IS-IS hello packets. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">metric_l1</span> - Level 1 metric for interface. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">metric_l2</span> - Level 2 metric for interface. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - IS-IS interface name <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">passive</span> - Set this interface as passive. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">priority_l1</span> - Level 1 priority. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">priority_l2</span> - Level 2 priority. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">status</span> - Enable the interface for IS-IS. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">status6</span> - Enable/disable interface for ipv6 IS-IS. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            <li> <span class="li-head">wide_metric_l1</span> - Level 1 wide metric for interface. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">wide_metric_l2</span> - Level 2 wide metric for interface. <span class="li-normal">type: int</span> </li>
            </ul>
        <li> <span class="li-head">is_type</span> - IS-type. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2-only</span> </li>
        <li> <span class="li-head">log_neighbour_changes</span> - Enable logging of ISIS neighbour"s changes <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">lsp_gen_interval_l1</span> - Minimum interval for level 1 LSP regenerating. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lsp_gen_interval_l2</span> - Minimum interval for level 2 LSP regenerating. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">lsp_refresh_interval</span> - LSP refresh time in seconds. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">max_lsp_lifetime</span> - Maximum LSP lifetime in seconds. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">metric_style</span> - Use old-style (ISO 10589) or new-style packet formats. <span class="li-normal">type: str</span> <span class="li-normal">choices: narrow, wide, transition</span> </li>
        <li> <span class="li-head">net</span> - IS-IS net configuration. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - ISIS net ID <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">net</span> - isis net xx.xxxx. ... .xxxx.xx <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">overload_bit</span> - Signal other routers not to use us in SPF. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">redistribute</span> - IS-IS redistribute protocols. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">level</span> - level. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2</span> </li>
            <li> <span class="li-head">metric</span> - metric. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">metric_type</span> - metric type. <span class="li-normal">type: str</span> <span class="li-normal">choices: external, internal</span> </li>
            <li> <span class="li-head">protocol</span> - protocol name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">routemap</span> - routemap name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">redistribute6</span> - IS-IS redistribute v6 protocols. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">level</span> - level. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2</span> </li>
            <li> <span class="li-head">metric</span> - metric. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">protocol</span> - protocol name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">routemap</span> - routemap name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">status</span> - status. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
            </ul>
        <li> <span class="li-head">redistribute6_l1</span> - Redistribute level 1 v6 routes into level 2. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">redistribute6_l1_list</span> - Access-list for redistribute v6 routes from l1 to l2. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">redistribute_l1</span> - Redistribute level 1 routes into level 2. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">redistribute_l1_list</span> - Access-list for redistribute l1 to l2. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">router_id</span> - Router ID. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">spf_interval_exp_l1</span> - Level 1 SPF minimum calculation delay in secs. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">spf_interval_exp_l2</span> - Level 2 SPF minimum calculation delay in secs. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">summary_address</span> - IS-IS summary addresses. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Summary address entry id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">level</span> - Level. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2</span> </li>
            <li> <span class="li-head">prefix</span> - prefix. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">summary_address6</span> - IS-IS summary ipv6 addresses. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Summary address entry id. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">level</span> - Level. <span class="li-normal">type: str</span> <span class="li-normal">choices: level-1-2, level-1, level-2</span> </li>
            <li> <span class="li-head">prefix6</span> - IPv6 prefix <span class="li-normal">type: str</span> </li>
            </ul>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: ISIS configuration.
      fortinet.fortiswitch.fortiswitch_router_isis:
          router_isis:
              auth_keychain_area: "<your_own_value> (source router.key-chain.name)"
              auth_keychain_domain: "<your_own_value> (source router.key-chain.name)"
              auth_mode_area: "password"
              auth_mode_domain: "password"
              auth_password_area: "<your_own_value>"
              auth_password_domain: "<your_own_value>"
              auth_sendonly_area: "enable"
              auth_sendonly_domain: "enable"
              default_information_level: "level-1-2"
              default_information_level6: "level-1-2"
              default_information_metric: "13"
              default_information_metric6: "14"
              default_information_originate: "enable"
              default_information_originate6: "enable"
              ignore_attached_bit: "enable"
              interface:
                  -
                      auth_keychain_hello: "<your_own_value> (source router.key-chain.name)"
                      auth_mode_hello: "md5"
                      auth_password_hello: "<your_own_value>"
                      bfd: "enable"
                      bfd6: "enable"
                      circuit_type: "level-1-2"
                      csnp_interval_l1: "25"
                      csnp_interval_l2: "26"
                      hello_interval_l1: "27"
                      hello_interval_l2: "28"
                      hello_multiplier_l1: "29"
                      hello_multiplier_l2: "30"
                      hello_padding: "enable"
                      metric_l1: "32"
                      metric_l2: "33"
                      name: "default_name_34 (source system.interface.name)"
                      passive: "enable"
                      priority_l1: "36"
                      priority_l2: "37"
                      status: "enable"
                      status6: "enable"
                      wide_metric_l1: "40"
                      wide_metric_l2: "41"
              is_type: "level-1-2"
              log_neighbour_changes: "enable"
              lsp_gen_interval_l1: "44"
              lsp_gen_interval_l2: "45"
              lsp_refresh_interval: "46"
              max_lsp_lifetime: "47"
              metric_style: "narrow"
              net:
                  -
                      id: "50"
                      net: "<your_own_value>"
              overload_bit: "enable"
              redistribute:
                  -
                      level: "level-1-2"
                      metric: "55"
                      metric_type: "external"
                      protocol: "<your_own_value>"
                      routemap: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
              redistribute6:
                  -
                      level: "level-1-2"
                      metric: "62"
                      protocol: "<your_own_value>"
                      routemap: "<your_own_value> (source router.route-map.name)"
                      status: "enable"
              redistribute6_l1: "enable"
              redistribute6_l1_list: "<your_own_value> (source router.access-list6.name)"
              redistribute_l1: "enable"
              redistribute_l1_list: "<your_own_value> (source router.access-list.name)"
              router_id: "<your_own_value>"
              spf_interval_exp_l1: "71"
              spf_interval_exp_l2: "72"
              summary_address:
                  -
                      id: "74"
                      level: "level-1-2"
                      prefix: "<your_own_value>"
              summary_address6:
                  -
                      id: "78"
                      level: "level-1-2"
                      prefix6: "<your_own_value>"


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
