:source: fortiswitch_system_accprofile.py

:orphan:

.. fortiswitch_system_accprofile:

fortiswitch_system_accprofile -- Configure system administrative access group in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and accprofile category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_accprofile</td>
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
    <li> <span class="li-head">system_accprofile</span> - Configure system administrative access group. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">admingrp</span> - Administrative access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">alias_commands</span> - Alias commands (or groups of commands) that can be used by this profile. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">command_name</span> - Alias command or group name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">exec_alias_grp</span> - Permission to execute alias commands. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">loggrp</span> - Logging access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write, w, r, rw</span> </li>
        <li> <span class="li-head">mntgrp</span> - Critical system maintenance access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">name</span> - Profile name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">netgrp</span> - Network access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">pktmongrp</span> - Packet and flow capture functionality. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">routegrp</span> - Routing access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">swcoregrp</span> - Switch core access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">swmonguardgrp</span> - Switch monitor and guard feature permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">sysgrp</span> - System access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        <li> <span class="li-head">utilgrp</span> - Utilities access permission. <span class="li-normal">type: str</span> <span class="li-normal">choices: none, read, read-write</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Configure system administrative access group.
      fortinet.fortiswitch.fortiswitch_system_accprofile:
          state: "present"
          system_accprofile:
              admingrp: "none"
              alias_commands:
                  -
                      command_name: "<your_own_value> (source system.alias.command.name system.alias.group.name)"
              exec_alias_grp: "none"
              loggrp: "none"
              mntgrp: "none"
              name: "default_name_9"
              netgrp: "none"
              pktmongrp: "none"
              routegrp: "none"
              swcoregrp: "none"
              swmonguardgrp: "none"
              sysgrp: "none"
              utilgrp: "none"


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
