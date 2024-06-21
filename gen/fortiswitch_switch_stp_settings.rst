:source: fortiswitch_switch_stp_settings.py

:orphan:

.. fortiswitch_switch_stp_settings:

fortiswitch_switch_stp_settings -- Switch-global stp settings in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify switch_stp feature and settings category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_switch_stp_settings</td>
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
    <li> <span class="li-head">switch_stp_settings</span> - Switch-global stp settings. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">flood</span> - Enable/disable stp bpdu flood. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">forward_time</span> - Forwarding delay. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">hello_time</span> - Hello time. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">max_age</span> - Maximum aging time. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">max_hops</span> - Maximum number of hops. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">mclag_stp_bpdu</span> - MCLAG STP bpdu. <span class="li-normal">type: str</span> <span class="li-normal">choices: both, single</span> </li>
        <li> <span class="li-head">mclag_stp_mac</span> - MCLAG STP mac address. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">pending_timer</span> - Pending time. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">revision</span> - Stp revision. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable spanning tree. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Switch-global stp settings.
      fortinet.fortiswitch.fortiswitch_switch_stp_settings:
          switch_stp_settings:
              flood: "enable"
              forward_time: "4"
              hello_time: "5"
              max_age: "6"
              max_hops: "7"
              mclag_stp_bpdu: "both"
              mclag_stp_mac: "<your_own_value>"
              name: "default_name_10"
              pending_timer: "11"
              revision: "12"
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
