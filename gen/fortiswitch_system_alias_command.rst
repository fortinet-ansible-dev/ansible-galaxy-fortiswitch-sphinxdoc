:source: fortiswitch_system_alias_command.py

:orphan:

.. fortiswitch_system_alias_command:

fortiswitch_system_alias_command -- Alias command definitions in Fortinet's FortiSwitch
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 1.0.0

.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module is able to configure a FortiSwitch device by allowing the user to set and modify system_alias feature and command category. Examples include all parameters and values need to be adjusted to datasources before usage. Tested with FOS v7.0.0



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
 <td>fortiswitch_system_alias_command</td>
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
    <li> <span class="li-head">system_alias_command</span> - Alias command definitions. <span class="li-normal">type: dict</span> </li>
        <ul class="ul-self">
        <li> <span class="li-head">attribute</span> - Attribute which can be retreived or modified. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">command</span> - Script command template (use $1 for user argument). <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">description</span> - Command description and/or help message. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">limit_shown_attributes</span> - Enable/disable limiting of config displayed in show and get. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
        <li> <span class="li-head">name</span> - Alias name. <span class="li-normal">type: str</span> <span class="li-required">required: true</span> </li>
        <li> <span class="li-head">path</span> - Path to configuration object or table. <span class="li-normal">type: str</span> </li>
        <li> <span class="li-head">permission</span> - Allow read and write operations, or only read operations on this path. <span class="li-normal">type: str</span> <span class="li-normal">choices: read, read-write</span> </li>
        <li> <span class="li-head">read_only_attributes</span> - Additional attributes allowed in get/show output when limit-shown-attributes is enabled. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">attribute_name</span> - Attribute name. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">script_arguments</span> - Optional meta-data and control values for script arguments. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">allowed_values</span> - Values to limit this argument to. <span class="li-normal">type: list</span> </li>
                <ul class="ul-self">
                <li> <span class="li-head">value</span> - Allowed value. <span class="li-normal">type: str</span> </li>
                </ul>
            <li> <span class="li-head">help</span> - A help message for the argument. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">id</span> - Argument ID. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">name</span> - Display name for the argument. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">optional</span> - Enable/disable the option to omit this argument. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">range</span> - Enable/disable the option to pass a range, or list, of values for this argument. <span class="li-normal">type: str</span> <span class="li-normal">choices: disable, enable</span> </li>
            <li> <span class="li-head">range_delay</span> - When running against a range of values, delay this many seconds between values when executing. <span class="li-normal">type: int</span> </li>
            <li> <span class="li-head">table_path</span> - Path to configuration object or table. <span class="li-normal">type: str</span> </li>
            <li> <span class="li-head">type</span> - Argument data type. <span class="li-normal">type: str</span> <span class="li-normal">choices: string, integer, table-id</span> </li>
            </ul>
        <li> <span class="li-head">table_entry_create</span> - Allow/prevent this script from creating new entries in config tables. <span class="li-normal">type: str</span> <span class="li-normal">choices: allow, deny</span> </li>
        <li> <span class="li-head">table_ids_allowed</span> - Table entries this command is limited to. <span class="li-normal">type: list</span> </li>
            <ul class="ul-self">
            <li> <span class="li-head">entry_id</span> - Entry ID. <span class="li-normal">type: str</span> </li>
            </ul>
        <li> <span class="li-head">table_listing</span> - Allow/prevent listing of all entries in the config table. <span class="li-normal">type: str</span> <span class="li-normal">choices: allow, deny</span> </li>
        <li> <span class="li-head">type</span> - Command type to alias. <span class="li-normal">type: str</span> <span class="li-normal">choices: configuration, script</span> </li>
        </ul>
    </ul>


Examples
--------

.. code-block:: yaml+jinja
    
    - name: Alias command definitions.
      fortinet.fortiswitch.fortiswitch_system_alias_command:
          state: "present"
          system_alias_command:
              attribute: "<your_own_value>"
              command: "<your_own_value>"
              description: "<your_own_value>"
              limit_shown_attributes: "disable"
              name: "default_name_7"
              path: "<your_own_value>"
              permission: "read"
              read_only_attributes:
                  -
                      attribute_name: "<your_own_value>"
              script_arguments:
                  -
                      allowed_values:
                          -
                              value: "<your_own_value>"
                      help: "<your_own_value>"
                      id: "16"
                      name: "default_name_17"
                      optional: "disable"
                      range: "disable"
                      range_delay: "20"
                      table_path: "<your_own_value>"
                      type: "string"
              table_entry_create: "allow"
              table_ids_allowed:
                  -
                      entry_id: "<your_own_value>"
              table_listing: "allow"
              type: "configuration"


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
