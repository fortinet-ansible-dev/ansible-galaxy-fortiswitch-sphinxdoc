:source: fortiswitch_system_automation_trigger.py

:orphan:

.. fortiswitch_system_automation_trigger:

fortiswitch_system_automation_trigger -- Trigger for automation stitches in Fortinet's FortiSwitch
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system feature and automation_trigger category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_automation_trigger</td>
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
    <li> <span class="li-head">state</span> - Indicates whether to create or remove the object. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> <span class="li-normal">choices: present, absent</span> </li>
    <li> <span class="li-head">system_automation_trigger</span> - Trigger for automation stitches. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">event_type</span> - Event type. <span class="li-normal">type: str</span> <span class="li-normal">choices: config-change, event-log, reboot</span> </li>
        <li> <span class="li-head">fields</span> - Customized trigger field settings. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">id</span> - Entry ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">value</span> - Value. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">logid</span> - Log ID to trigger event. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">name</span> - Name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">trigger_day</span> - Day within a month to trigger. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trigger_frequency</span> - Scheduled trigger frequency . <span class="li-normal">type: str</span> <span class="li-normal">choices: hourly, daily, weekly, monthly</span> </li>
        <li> <span class="li-head">trigger_hour</span> - Hour of the day on which to trigger (0 - 23). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trigger_minute</span> - Minute of the hour on which to trigger (0 - 59). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">trigger_type</span> - Trigger type. <span class="li-normal">type: str</span> <span class="li-normal">choices: event-based, scheduled</span> </li>
        <li> <span class="li-head">trigger_weekday</span> - Day of week for trigger. <span class="li-normal">type: str</span> <span class="li-normal">choices: sunday, monday, tuesday, wednesday, thursday, friday, saturday</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Trigger for automation stitches.
      fortinet.fortiswitch.fortiswitch_system_automation_trigger:
          state: "present"
          system_automation_trigger:
              event_type: "config-change"
              fields:
                  -
                      id: "5"
                      name: "default_name_6"
                      value: "<your_own_value>"
              logid: "<your_own_value>"
              name: "default_name_9"
              trigger_day: "15"
              trigger_frequency: "hourly"
              trigger_hour: "11"
              trigger_minute: "29"
              trigger_type: "event-based"
              trigger_weekday: "sunday"


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
