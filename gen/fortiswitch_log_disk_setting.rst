:source: fortiswitch_log_disk_setting.py

:orphan:

.. fortiswitch_log_disk_setting:

fortiswitch_log_disk_setting -- Settings for local disk logging in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify log_disk feature and setting category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_log_disk_setting</td>
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
    <li> <span class="li-head">log_disk_setting</span> - Settings for local disk logging. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">diskfull</span> - Policy to apply when disk is full. <span class="li-normal">type: str</span> <span class="li-normal">choices: overwrite, nolog</span> </li>
        <li> <span class="li-head">drive_standby_time</span> - Power management timeout(0-19800 sec)(0 disable). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">full_final_warning_threshold</span> - Log full final warning threshold(3-100), the default is 95. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">full_first_warning_threshold</span> - Log full first warning threshold(1-98), the default is 75. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">full_second_warning_threshold</span> - Log full second warning threshold(2-99), the default is 90. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">log_quota</span> - Disk log quota. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">max_log_file_size</span> - Max log file size in MB before rolling (may not be accurate all the time). <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">report_quota</span> - Report quota. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">roll_day</span> - Days of week to roll logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: sunday, monday, tuesday, wednesday, thursday, friday, saturday</span> </li>
        <li> <span class="li-head">roll_schedule</span> - Frequency to check log file for rolling. <span class="li-normal">type: str</span> <span class="li-normal">choices: daily, weekly</span> </li>
        <li> <span class="li-head">roll_time</span> - Time to roll logs [hh:mm]. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">source_ip</span> - Source IP address of the disk log uploading. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">status</span> - Enable/disable local disk log. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">upload</span> - Whether to upload the log file when rolling. <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">upload_delete_files</span> - Delete log files after uploading . <span class="li-normal">type: str</span> <span class="li-normal">choices: enable, disable</span> </li>
        <li> <span class="li-head">upload_destination</span> - Server type. <span class="li-normal">type: str</span> <span class="li-normal">choices: ftp-server</span> </li>
        <li> <span class="li-head">upload_format</span> - Upload compact/text logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: compact, text</span> </li>
        <li> <span class="li-head">upload_ssl_conn</span> - Enable/disable SSL communication when uploading. <span class="li-normal">type: str</span> <span class="li-normal">choices: default, high, low, disable</span> </li>
        <li> <span class="li-head">uploaddir</span> - Log file uploading remote directory. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">uploadip</span> - IP address of the log uploading server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">uploadpass</span> - Password of the user account in the uploading server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">uploadport</span> - Port of the log uploading server. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">uploadsched</span> - Scheduled upload (disable=upload when rolling). <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">uploadtime</span> - Time of scheduled upload. <span class="li-normal">type: int</span> </li>
        <li> <span class="li-head">uploadtype</span> - Types of log files that need to be uploaded. <span class="li-normal">type: str</span> <span class="li-normal">choices: traffic, event, virus, webfilter, attack, spamfilter, dlp-archive, dlp, app-ctrl</span> </li>
        <li> <span class="li-head">uploaduser</span> - User account in the uploading server. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">uploadzip</span> - Compress upload logs. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Settings for local disk logging.
      fortinet.fortiswitch.fortiswitch_log_disk_setting:
          log_disk_setting:
              diskfull: "overwrite"
              drive_standby_time: "4"
              full_final_warning_threshold: "5"
              full_first_warning_threshold: "6"
              full_second_warning_threshold: "7"
              log_quota: "8"
              max_log_file_size: "9"
              report_quota: "10"
              roll_day: "sunday"
              roll_schedule: "daily"
              roll_time: "<your_own_value>"
              source_ip: "<your_own_value>"
              status: "enable"
              upload: "enable"
              upload_delete_files: "enable"
              upload_destination: "ftp-server"
              upload_format: "compact"
              upload_ssl_conn: "default"
              uploaddir: "<your_own_value>"
              uploadip: "<your_own_value>"
              uploadpass: "<your_own_value>"
              uploadport: "24"
              uploadsched: "disable"
              uploadtime: "26"
              uploadtype: "traffic"
              uploaduser: "<your_own_value>"
              uploadzip: "disable"


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
